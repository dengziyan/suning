<template>
    <section>
        <router-view></router-view>
        <ul class="footGuide">
            <li @click="change(0)">
                <router-link to="/like">
                    <img src="../assets/img/157543975265772267.png" alt="" v-if="show==0">
                    <img src="../assets/img/like1.png" alt="" v-else>
                    <span>猜你喜欢</span>
                </router-link>
            </li>
            <li @click="change(1)">
                <router-link to="/type">
                    <img src="../assets/img/type2.png"  alt="" v-if="show==1">
                    <img src="../assets/img/157562573743964714.png" alt="" v-else>
                    <span>分类</span>
                </router-link>
            </li>
            <li @click="change(2)">
                <router-link to="/menu">
                    <img src="../assets/img/menu2.png" alt="" v-if="show==2">
                    <img src="../assets/img/157543978244974042.png" alt="" v-else>
                    <span>必抢清单</span>
                </router-link>
            </li>
            <li @click="change(3)">
                <router-link to="/cart">
                    <img src="../assets/img/cart2.png" alt="" v-if="show==3">
                    <img src="../assets/img/157543979328589256.png" alt="" v-else>
                    <span>购物车</span>
                </router-link>
            </li>
            <li @click="change()">
                <router-link to="/my">
                    <img src="../assets/img/157543980229048220.png" alt="">
                    <span>我的易购</span>
                </router-link>
            </li>
        </ul>
    </section>
</template>

<script>
    export default {
        data () {
        return {
            show:0
         
        }
        },
        methods:{
            change(a){
                this.show=a         
            }
        }
  }
</script>
<style>
html{
        font-size: 24px;
    }
</style>

<style scoped>

     .footGuide{
        background: white;
        width: 100%;
        position: fixed;
        bottom: 0px;
        z-index: 99;
        list-style: none;
        flex-direction: row;
        display: flex;
        padding: 0px 20px 10px 20px;
        box-sizing: border-box;
     }
     .footGuide li{
        width: 20%;
        height: 2rem;
        background: #fff;
     }
     .footGuide li a{
        text-decoration: none;
        text-align: center;
        display: block;
     }
     .footGuide img{
        display: block;
        width: 47%;
        /* height: .96rem; */
        margin: .24rem auto 0;
     }
     .footGuide span{
        display: block;
        font-size: 0.5rem;
        line-height: .64rem;
        color: #666;
     }
     
     /* .router-link-exact-active img{
         background: red;
     } */
</style>

