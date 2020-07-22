<template>
    <div>
        <header>
            <span></span>
            <u></u>
            <div>
                <input type="text" placeholder="请搜索商品、店铺"
             value="手机">
            </div>           
            <i></i>
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
                <li>
                    <p>品牌</p>
                    <i></i>
                </li>
                <li>
                    <p>屏幕尺寸</p>
                    <i></i>
                </li>
                <li>
                    <p>机身内存</p>
                    <i></i>
                </li>
            </ul>
            <div class="shop">
                 <ul>
                    <li v-for="(v,i) in shoplist" :key="i">
                        <div class="left">
                            <img :src="v.imgsrc" alt="" />
                            
                        </div>
                        <div class="right">
                            <div class="detail">
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
                                <p>{{v.shop}}</p>
                            </div>

                        </div>
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
        top: 14px;
        left: 15%;
    }
     header i{
        background: url('../../assets/img/search-icon9.png') no-repeat;
        background-size: 100%;
        position: absolute;
        width: 20px;
        height: 20px;
        top: 12px;
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
    .choose li i{
        background: url('../../assets/img/icon.png') 
        -23px -12px no-repeat;
        position: absolute;
        width: 17px;
        height: 7px;
        top: 10px;
        right: 0px;
    }
    .choose li:nth-child(1){
        margin-left: 2%;
    }

    main .shop{
        padding: 10px;
        box-sizing: border-box;

    }
    .shop .left{
        float: left;
        width: 30%;
        margin-right: 5%;
    }
    .shop .left img{
        width: 100%;
    }
    .shop .right{
        float: left;
        width: 60%;
    }
    .right .detail h5{
        font-size: 15px;
        font-weight: normal;
        color: #734c01;

    }
    .right .detail p{
        font-size: 14px;
        color: #999;
        word-break: break-all;
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 1;
        
    }
   
    .right .size li{
        width: 30%;
        float: left;
        margin-right: 2%;
        background:#F9F9F9;
    }
    .right .size li b{
        font-size: 12px;
        font-weight: bold;
    }
    .right .size li p{
        font-size: 10px;
        color: #999;
    }
    .shop .comments{
        color: #999;
        margin-top:100px;
    }


</style>
