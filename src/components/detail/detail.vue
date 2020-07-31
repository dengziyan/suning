<template>
    <div>
        <header>
            <div class="icon">
                <span></span>
                <i></i>
            </div>           
        </header>
        <main>
            <div class="img">
                <span></span>
                <img src="../../assets/img/detail1.jpg" alt="">
                <i></i>
                
            </div>
            <div class="price">
                   <div class="left">
                       <span>￥<i>5499</i>.00</span>
                       <p><b>￥5999.00</b><i>月销12551件</i></p> 
                       
                   </div>
                   <div class="right">
                       <img src="../../assets/img/baiyi-logo.png" alt="">
                       <p>距结束02天</p>
                   </div>
                                   
            </div>
            <div class="detail">
                       <div class="sup">
                           <div class="supL">
                                <span>自营</span>
                                <h5>Apple iPhone 11 128G 紫色 移动联通电信4G全网通手机</h5>
                           </div>
                           <div class="supR">
                               <img src="../../assets/img/关注.png" alt="">
                           </div>                                                      
                       </div>
                       <div class="sub">
                           <p><i>【百亿补贴活动商品不参与贵就赔】强悍A13仿生，双摄超广角，
                               面部识别，多色可选，精彩每一天~</i><u>抢百亿补贴优惠>></u></p>
                       </div>                      
                   </div>  
            <!-- 榜单信息 -->
            <div class="listmsg">
                <div class="cell">
                    <span>榜单</span>
                    <u>此商品已入选『十款性能强劲不卡顿的旗舰手机』</u>
                </div>
                <div class="more">
                    <!-- <img src="../../assets/img/detail2.png" alt=""> -->
                    <u>可参加以下优惠活动</u>
                    <span>查看更多</span>
                </div>
                <div class="sale">
                    <div class="sale-left">
                        <p>促销</p>
                    </div>
                    <div class="sale-right">
                        <p>
                            <span>实名领券</span>
                            <i>实名认证领10元支付券</i>
                        </p>
                        <p>
                            <span>限量赠</span>
                            <i>1-100000名送赠品（赠完即止）</i>
                        </p>                       
                    </div>                    
                </div>  
                <div class="coupons">   
                    <div class="coupons-left">          
                        <p>刮券</p>
                    </div>
                    <div class="coupons-right">
                        <p>
                            <span>云钻刮券</span>
                            <i>100%刮中券，最高50元无敌券</i>
                        </p>
                    </div>
                </div> 
 
                         
            </div>
            <!-- 以旧换新 -->   
            <div class="renew">
                <img src="../../assets/img/renew1.png" alt="">
                <u>1000元至高补贴，点此领取</u>
                <span>以旧换新</span>
            </div>
            <!-- 地址 -->
            <div class="place">
                <div class="part">
                    <i>已选</i>
                    <u>白色，128G 1件 可选增值服务</u>
                    <img src="../../assets/img/next.png" alt="">
                </div>
                <div class="part send">
                    <i>送至</i>
                    <u>广东 广州 荔湾区 全区</u>
                    <img src="../../assets/img/next.png" alt="">
                </div>
                <div class="part service">
                    <i>服务</i>
                    <u><b>苏宁发货</b><b>自提</b><b>商品报关说明</b>  </u>
                    <img src="../../assets/img/next.png" alt="">
                </div>
            </div>
            <div class="image">
                <img src="../../assets/img/img1.jpg" alt="">
                <img src="../../assets/img/img2.jpg" alt="">
                <img src="../../assets/img/img3.jpg" alt="">
                <img src="../../assets/img/img4.jpg" alt="">
                <img src="../../assets/img/img5.jpg" alt="">
                <img src="../../assets/img/img6.jpg" alt="">
                <img src="../../assets/img/img7.jpg" alt="">
                <img src="../../assets/img/img8.jpg" alt="">
                <img src="../../assets/img/img9.jpg" alt="">
            </div>
        </main>
    </div>
</template>   
<script>

</script>   
<style scoped>
    header{
        background: linear-gradient(180deg,rgba(0,0,0,.1),transparent);
        /* height:30px ; */
        
            
    }
    header .icon{
        position: relative;
        width: 100%;
        background: pink;
        z-index: 100;
        position: fixed;
    }
    header span{
        background: url('../../assets/img/小于.png') no-repeat;
        background-size: 89%;
        width: 30px;
        height: 30px;
        top:4px;
        left:10px;
        position: absolute;
    }
    header i{
        background: url('../../assets/img/nav-more3.png') no-repeat;
        background-size: 89%;
        width: 30px;
        height: 30px;
        top:4px;
        right:10px;
        position: absolute;
        z-index: 99;
    }
    main .img{
        width: 100%;
        height: 320px;
        overflow: hidden;
    }
    .img img{
        width: 100%;
        padding-bottom:100%;
    }
    main .price{
        background: url('../../assets/img/baiyi-baofa.png') no-repeat;
        background-size: 100%;
        /* position: absolute; */
        width: 100%;
        height: 54px;
        top: 0px;
        left: 0px;
        /* margin-top: 320px; */
        color:white;
    }
    .price .left{
        float: left;
        margin-left: 10px;
        font-size: 12px;
    } 
    .left p b{
        font-size: 12px;
    }
    .left p i{
        font-size: 12px;
        padding-left: 6px;
    }
    .left span{
        font-size: 12px;
    }
    .left span i{
        font-size: 22px;
        /* font-weight: bold; */
    }
    .price .right{
        float: right;
    }
    .right img{
        width: 70px;
        height: 20px;
        margin-right: 5px;
        margin-top:10px;
    }
    .right p{
        font-size: 6px;
        padding-right: 50px;
    }
    main{
        /* background: #F2F2F2; */
    }
    main .detail{
        box-sizing: border-box;
        padding:10px;
        border-bottom: 4px solid #F2F2F2;
    }
    .detail .sup{
        font-size:14px;
        color: #222;
        display: flex;
        flex-direction: row;
        width: 100%;
        padding-bottom: 10px;
        
    }
    .sup .supL{
        width: 85%;
    }
    .sup .supR{
        width: 15%;
        text-align: center;
    }
    .sup .supR img{
        width: 66%;
    }
    .sup span{
        display: inline-block;
        background: #fc0;
        color: #222;
        font-size: 10px;
        border-radius: 3px;
    }
    .sup h5{
        display: inline;
    }

    .detail .sub{
        font-size: 12px;
    }
    .sub i{
        color: rgb(153, 153, 153);
    }
    .sub u{
        color: rgb(255, 68, 34);
    }
    /* 榜单信息 */
    main .listmsg{
        font-size: 10px;
        /* padding-top: 180px; */
        padding-left: 10px;
        padding-right: 10px;

    }   
    .listmsg .cell{
        color: #999;
        display: flex;
        flex-direction: row;
        line-height: 30px;
        justify-content: space-between;
    }
    .listmsg .cell span{
        padding-right:15px;
    }
    .listmsg .cell u{
        color: #222;
        font-size: 11px;
        position: relative;
        padding-right: 20px;
    } 
    .listmsg .cell u::after{
        position: absolute;
        width: 20px;
        height: 20px;
        content: "\020";
        background-size: 10%;
        background: url('../../assets/img/next.png') no-repeat;
        background-size: contain;
        top: 5px;
    }
    .listmsg .more{
        line-height: 30px;
        display: flex;
        flex-direction: row;
        align-content: center;
        justify-content: space-between;
    }
    .listmsg .more u{
        color: #333;
        /* padding-right: 131px; */
        position: relative;
        padding-left: 15px;
    }
    .listmsg .more u::before{
        position: absolute;
        width: 13px;
        height: 13px;
        left: 0px;
        top: 6px;
        content: "\020";
        background: url('../../assets/img/detail2.png');
        background-size: contain;
    }
    .listmsg .more span{
        color: #999;
        padding-right: 20px;
        
    }
    .listmsg .more span::after{
        position: absolute;
        width: 20px;
        height: 20px;
        content: "\020";
        background: url('../../assets/img/next.png');
        background-size: contain;
    }
    .listmsg .sale,.listmsg .coupons{
        display: flex;
        flex-direction:row ;
    }
    .listmsg .coupons{
        display: flex;
        flex-direction:row ;
    }
    .sale .sale-left,.coupons .coupons-left{
        color: #999;
        padding-right: 10px;
    }
    .sale span,.coupons span{
        border: 1px solid #fb0;
        background-color: #fefbee;
        border-radius: 3px;
        padding: 0px 3px;
    }
    .sale-right p,.coupons-right p{
        line-height: 22px;
    }

    /* 以旧换新 */
    main .renew{
        justify-content: space-around;
        padding-right:20px;
        align-content: center;
        display: flex;
        line-height: 35px;
        background: white;
        border-top:5px solid #F2F2F2;
        border-bottom:5px solid #F2F2F2;
    }
    .renew img{
        margin-top: 8px;
        height: 16px;
    }
    .renew u{
        font-size: 12px;
        width: 50%;
        overflow: hidden;
        text-overflow: ellipsis;
        display: inline-block;
        width: 160px;
        white-space: nowrap;
    }
    .renew span{
        position: relative;
        color: #999;
        font-size: 10px;

    }
    .renew span::after{
        position: absolute;
        width: 20px;
        height: 20px;
        top:5px;
        content: "\020";
        background: url('../../assets/img/next.png');
        background-size: contain;
    }
    main .place{
        background: white;
        padding: 0px 10px;
        
        border-bottom:5px solid #F2F2F2; ;
    }
    .place .part{
        position: relative;
        align-content: center;
        display: flex;
        line-height: 35px;       
    }
    .place .part i{
        color: #999;
        padding-right: 10px;
        font-size:10px ;
    }
    .place .part u{
        color: #222;
        font-size:10px ;
    }
    .place .part img{
        position: absolute;
        width: 20px;
        height: 20px;
        right:0px;
        top: 10px;
    }
    .place .send u{
        position: relative;
        padding-left: 10px;
    }
    .place .send u::before{
        position: absolute;
        width: 20px;
        height: 20px;
        top:11px;
        left: -1px;
        content: "\020";
        background: url('../../assets/img/place.png') no-repeat;
        background-size: 40%;
    }
    .place .service b{
        padding-left: 9px;
        padding-right: 15px;
        position: relative;
    }
    .place .service b::before{
        position: absolute;
        width: 20px;
        height: 20px;
        top: 3px;
        left: 0px;
        content: "\020";
        background: url('../../assets/img/get.png') no-repeat;
        background-size: 45%;
    }
    
    main  .image{
        width: 100%;
    }
    .image img{
        width: 100%;
    }
        
</style>