<template>
    <div class="recommended-author">
        <div class="title" @click="rotate">
            <span>推荐作者</span>
            <a href="javascript:void (0)">
                <i ref="change" class="fa fa-refresh"></i> 换一批
            </a>
        </div>
        <ul class="list">
            <li>
                <nuxt-link class="list-avatar" to="/author">
                    <img src="../assets/img/recommended-author-tag1.png" alt="">
                </nuxt-link>
                <nuxt-link class="add" to="/author">
                    <i class="fa fa-plus"></i>关注
                </nuxt-link>
                <nuxt-link class="list-author" to="/author">
                    简宝玉
                </nuxt-link>
                <p>写了70.6k字 · 10.9k喜欢</p>
            </li>
            <li>
                <nuxt-link class="list-avatar" to="/author">
                    <img src="../assets/img/recommended-author-tag2.png" alt="">
                </nuxt-link>
                <nuxt-link class="add" to="/author">
                    <i class="fa fa-plus"></i>关注
                </nuxt-link>
                <nuxt-link class="list-author" to="/author">
                    简书出版
                </nuxt-link>
                <p>写了306.7k字 · 23.5k喜欢</p>
            </li>
            <li>
                <nuxt-link class="list-avatar" to="/author">
                    <img src="../assets/img/recommended-author-tag3.jpeg" alt="">
                </nuxt-link>
                <nuxt-link class="add" to="/author">
                    <i class="fa fa-plus"></i>关注
                </nuxt-link>
                <nuxt-link class="list-author" to="/author">
                    雪发如糖
                </nuxt-link>
                <p>写了226.2k字 · 6k喜欢</p>
            </li>
            <li>
                <nuxt-link class="list-avatar" to="/author">
                    <img src="../assets/img/recommended-author-tag4.jpg" alt="">
                </nuxt-link>
                <nuxt-link class="add" to="/author">
                    <i class="fa fa-plus"></i>关注
                </nuxt-link>
                <nuxt-link class="list-author" to="/author">
                    遛遛心情的溜妈
                </nuxt-link>
                <p>写了306.2k字 · 1.4k喜欢</p>
            </li>
            <li>
                <nuxt-link class="list-avatar" to="/author">
                    <img src="../assets/img/recommended-author-tag5.jpg" alt="">
                </nuxt-link>
                <nuxt-link class="add" to="/author">
                    <i class="fa fa-plus"></i>关注
                </nuxt-link>
                <nuxt-link class="list-author" to="/author">
                    名贵的考拉熊
                </nuxt-link>
                <p>写了160.5k字 · 12.1k喜欢</p>
            </li>
        </ul>
        <nuxt-link class="see-more" to="/see/123">
            查看全部
            <i class="fa fa-angle-right"></i>
        </nuxt-link>
    </div>
</template>
<script>
    import Nuxt from "../.nuxt/components/nuxt";
    export default {
        components: {Nuxt},
        data(){
            return{
                deg:0
            }
        },
        methods:{
            rotate:function () {
                this.deg = this.deg + 360;
                this.$refs.change.style.transform = `rotate(${this.deg}deg)`
            }
        }
    }
</script>
<style>
    .recommended-author{
        width: 100%;
        height: 330px;
        margin-bottom: 20px;
        position: relative;
    }
    /*推荐作者 头部*/
    .recommended-author .title{
        width: 100%;
        height: 19px;
        line-height: 19px;
    }
    .recommended-author .title span{
        font-size: 14px;
        color: #969696;
    }
    .recommended-author .title a{
        float: right;
        display: inline-block;
        font-size: 14px;
        color: #969696!important;
    }
    .recommended-author .title a i{
        transition: ease .5s;
    }
    /*推荐作者主体*/
    .recommended-author .list{
        width: 100%;
        height: 295px;
        margin: 0 0 20px 0;
    }
    .recommended-author .list li{
        width: 100%;
        height: 47px;
        margin-top: 15px;
    }
    .recommended-author .list li .list-avatar{
        width: 48px;
        height: 48px;
        display: block;
        border: 1px solid #ccc;
        border-radius: 50%;
        float: left;
        margin-right: 10px;
        overflow: hidden;
    }
    .recommended-author .list li .list-avatar img{
        width: 100%;
        height: 100%;
    }
    .recommended-author .list li .add{
        width: 39px;
        height: 17px;
        display: block;
        float: right;
        margin-top: 5px;
        padding: 0;
        font-size: 13px;
        color: #42c02e!important;
    }
    .recommended-author .list li .list-author{
        padding-top: 5px;
        margin-right: 60px;
        font-size: 14px;
        display: block;
    }
    .recommended-author .list li P{
        margin-top: 2px;
        font-size: 12px;
        color: #969696;
        margin: 0 0 10px;
    }
    /*推荐作者尾部*/
    .recommended-author .see-more{
        position: absolute;
        padding: 7px 7px 7px 12px;
        left: 0;
        width: 100%;
        font-size: 13px;
        color: #787878!important;
        background-color: #f7f7f7;
        border: 1px solid #dcdcdc;
        border-radius: 4px;
        text-align: center;
        margin-top: 20px;
    }
</style>