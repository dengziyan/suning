<template>
    <div>
        <header>
            <span></span>
            <u></u>
            <div>
                <input type="text" placeholder="请搜索商品、店铺"
             value="手机">
            </div>           
            <router-link to="/type"><i></i></router-link>
        </header>
        <main>
            <ul class="rule">
                <li>综合</li>
                <li>销量</li>
                <li>价格</li>
                <li>筛选</li>
            </ul>
            <ul class="choose">
                <li>
                    <p> 苏宁服务</p>                 
                </li>
                <li class="span">
                    <p>品牌</p>
                </li>
                <li class="span">
                    <p>屏幕尺寸</p>
                </li>
                <li class="span">
                    <p>机身内存</p>
                </li>
            </ul>
            <div class="shop">
                 <ul>
                    <li class="goods"   v-for="(v,i) in shoplist" :key="i">
                        <router-link to="/detail">
                            <div class="left">
                                <img :src="v.imgsrc" alt="" />                           
                            </div>
                            <div class="right">
                                <div class="detail">
                                    
                                        <span>自营</span>
                                        <h5>{{v.name}}</h5>
                                    
                                    <p>{{v.attribute}}</p>
                                </div>                           
                                <ul class="size">
                                    <li v-for="(a,i) in v.dec" :key="i">
                                        <b>{{a.b}}</b>
                                        <p>{{a.p}}</p>
                                    </li>
                                </ul>
                                <div class="comments">
                                    <P>
                                        <span>{{v.comSpan1}}</span>
                                        <span>{{v.comSpan2}}</span>
                                    </P>
                                    <p>
                                        <span class="shopName">{{v.shop}}</span>
                                        <!-- <span>进店></span> -->
                                    </p>
                                </div>
                            </div>
                        </router-link>
                    </li>       
                </ul>
            </div> 
        </main>
    </div>
</template>

<script>
export default{
		data(){
			return{
				shoplist:{}		
			}
		},
		methods:{
			forward(){
				this.$router.push('/recommend');
			}
		},
		 mounted(){
		 	
		   this.$http.get('./data/shoplist.json')
		   .then((response)=> {
		     console.log(response.data);
			 this.shoplist=response.data.shoplist;			
		   })
		   .catch(function (error) {
		     // handle error
		     console.log(error);
		   })
		   .then(function () {
		     // always executed
		   });
		   
		}
	}
</script>  

<style scoped>
    header{
        padding-top: 8px;
        padding-bottom: 8px;
        width: 100%;
        text-align: center;
        /* height: 50px; */
        border-bottom: 2px solid #EEEEEE;
    }

    header span{
        background: url('');
    }
    header u{
        background: url('../../assets/img/search-icon3.png') no-repeat;
        background-size: 60%;
        position: absolute;
        width: 20px;
        height: 20px;
        top: 22px;
        left: 15%;
    }
     header i{
        background: url('../../assets/img/search-icon9.png') no-repeat;
        background-size: 100%;
        position: absolute;
        width: 20px;
        height: 20px;
        top: 18px;
        right: 5%;
    }
    
    header input{
        box-sizing: border-box;
        background:#EEEEEE;
        border: none;
        width: 74%;
        height: 30px;
        border-radius: 5px;
        padding-left:26px;
    }
    main .rule{
        display: flex;
        flex-direction: row;
        font-size: 14px;
        color:#333;
        box-sizing: border-box;
        border-bottom: 1px solid #EEEEEE;
    }
    .rule li{
        width: 25%;
        text-align: center;
        padding: 10px;
    }
    main .choose{
        padding-top: 8px;
        display: flex;
        flex-direction: row;
        font-size: 12px;
        color:#333;
        box-sizing: border-box;
    }
     .choose li{
        background: #eeeeee;
        width: 23%;
        margin-right:2%;
        text-align: center;
        padding: 6px 8px;
        position: relative;
    }
    .choose .span p{
        position: relative;
    }
    .choose .span p::after{
        content: " ";
        background: url('../../assets/img/icon.png') 
        -24px -15px no-repeat;    
        position: absolute;
        width: 8px;
        height: 4px;
        top: 7px;
        right: -3px;
    }
    /* .choose li i{
        background: url('../../assets/img/icon.png') 
        -24px -15px no-repeat;    
        position: absolute;
        width: 8px;
        height: 4px;
        top: 12px;
        right: 12px;
    } */
    .choose li:nth-child(1){
        margin-left: 2%;
    }

    main .shop{
        padding: 10px;
        box-sizing: border-box;

    }
    main .shop .goods{
        /* margin-bottom: 30px; */
    }
    .shop .left{
        float: left;
        width: 30%;
        margin-right: 5%;
        padding-top: 20px;
    }
    .shop .left img{
        width: 100%;
    }
    .shop .right{
        float: left;
        width: 60%;
        border-bottom: 1px solid #EEEEEE;
        padding-bottom: 10px;
        padding-top: 20px;
    }
    .right .detail span{
        display: inline-block;
        border: 1px solid #f60;
        color: #f60;
        font-size: 12px;
        padding: 1px;
        border-radius: 3px;

    }
    .right .detail h5{
        font-size: 12px;
        font-weight: normal;
        color: #734c01;
        display: inline;
    }
    .right .detail p{
        font-size: 12px;
        color: #999;
        word-break: break-all;
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 1;
        
    }
   
    .right .size li{
        margin-top: 10px;
        width: 26%;
        float: left;
        margin-right: 2%;
        background:#F9F9F9;
        text-align: center;
    }
    .right .size li b{
        font-size: 12px;
        font-weight: bold;
        color:#353D44;
    }
    .right .size li p{
        font-size: 10px;
        color: #999;
    }
    .shop .comments{
        color: #999;
        margin-top:90px;
        font-size: 14px;
    }
    .shop .comments span{
        padding-right:10px;
        font-size: 12px;
    }
    .shop .comments .shopName{
        font-size: 12px;
        position: relative;
        word-break: break-all;
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 1;
        display: inline-block;
        padding-right: 44px;
        width: 136px;
        white-space: nowrap;
    }
    .shop .comments .shopName::after{
        position: absolute;
        content: '进店>';
        width: 40px;
        font-size: 12px;
        top: 0px;
        right: -8px;
    }


</style>
