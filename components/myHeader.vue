<template>
    <div>
        <nav class="navbar navbar-default nav-fixed-top">
            <div class="width-limit">
               <!--logo-->
                <nuxt-link to="/">
                    <img class="nav-logo" src="../assets/img/nav-logo-4c7bbafe27adc892f3046e6978459bac.png" alt="">
                </nuxt-link>
                <!--写文章-->
                <nuxt-link to="/create" class="btn write-btn">
                    <i class="fa fa-pencil">写文章</i>
                </nuxt-link>
                <!--登录注册按钮-->
                <nuxt-link to="/sign-up" class="btn sign-up">注册</nuxt-link>
                <nuxt-link to="/sign-in" class="btn sign-in">登录</nuxt-link>
                <!--如果用户登录那么显示用户头像-->
                <div style="display: none" class="user" @mouseleave="userShow=false">
                    <div class="drop-down" @mouseover="userShow=true">
                        <nuxt-link to="/users" class="avatar">
                            <img src="../assets/img/default-img.jpg" alt="">
                        </nuxt-link>
                    </div>
                    <div class="drop-menu" v-show="userShow">
                        <ul>
                            <li>
                                <nuxt-link to="/">
                                    <i class="fa fa-user"></i>我的主页
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/">
                                    <i class="fa fa-bookmark"></i>收藏的文章
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/">
                                    <i class="fa fa-heart"></i>喜欢的文章
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/">
                                    <i class="fa fa-cog"></i>设置
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/">
                                    <i class="fa fa-sign-out"></i>退出
                                </nuxt-link>
                            </li>
                        </ul>
                    </div>
                </div>
                <!--导航栏按钮-->
                <div class="my-container">
                    <ul class="nav-list">
                        <li class="active nav-list-li">
                            <nuxt-link to="/">
                                <i class="fa fa-compass nav-list-i"></i>
                                <span class="nav-list-span">发现</span>
                            </nuxt-link>
                        </li>
                        <li class="nav-list-li">
                            <nuxt-link to="/">
                                <i class="fa fa-book nav-list-i"></i>
                                <span class="nav-list-span">关注</span>
                            </nuxt-link>
                        </li>
                        <!--显示隐藏消息-->
                        <li class="nav-list-li" @mouseover="messageShow=true" @mouseleave="messageShow=false">
                            <nuxt-link to="/">
                                <i class="fa fa-bell-o nav-list-i"></i>
                                <span class="nav-list-span">消息</span>
                            </nuxt-link>
                            <div class="drop-menu" v-show="messageShow">
                                <ul>
                                    <li>
                                        <nuxt-link to="/">
                                            <i class="fa fa-comment-o"></i><span class="messageshow-span">评论</span>
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/">
                                            <i class="fa fa-envelope-o"></i><span class="messageshow-span">简信</span>
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/">
                                            <i class="fa fa-upload"></i><span class="messageshow-span">投稿请求</span>
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/">
                                            <i class="fa fa-heart-o"></i><span class="messageshow-span">喜欢和赞</span>
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/">
                                            <i class="fa fa-user-plus"></i><span class="messageshow-span">关注</span>
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/">
                                            <i class="fa fa-ellipsis-h"></i><span class="messageshow-span">其他提醒</span>
                                        </nuxt-link>
                                    </li>
                                </ul>
                            </div>
                        </li>
                        <!--伸缩型输入框-->
                        <li class="search nav-list-li">
                            <form action="" method="post">
                                <transition>
                                <input @focus="bgShow = true" @blur="bgShow = false" type="text" placeholder="搜索"></transition>
                                <nuxt-link to="/search" :class="{active:bgShow}" class="search-btn"><i class="fa fa-search"></i></nuxt-link>
                            </form>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</template>
<script>
    import Nuxt from "../.nuxt/components/nuxt";
    export default {
        components: {Nuxt},
        name:'myHeader',//给组件命名
        data(){
            return{
                userShow:false,
                messageShow:false,
                bgShow:false
            }
        }
    }
</script>
<style>
    nav{
        height: 56px;
        width: 100%;
    }
    .navbar{
        padding: 0;
        border-bottom: 1px solid #e7e7e7;
        margin-bottom: 20px;
        background-color: #fff;
    }
    .nav-fixed-top{
        position: fixed;
        top: 0;
        left: 0;
        z-index: 65454;
    }
    nav .width-limit{
        width: 1440px;
        min-width: 785px;
        margin: 0 auto;
    }
    nav .nav-logo{
        float: left;
        height: 56px;
        padding: 0;
    }
    nav a.write-btn{
        float: right;
        width: 100px;
        height: 40px;
        margin: 8px 15px 0;
        font-size: 16px;
        background-color: #ea6f5a;
        color: #fff!important;
        border-radius: 20px;
    }
    nav a.write-btn:hover{
        color: #fff!important;
        opacity: .8;
    }
    nav a.sign-in{
        float: right;
        width: 100px;
        height: 40px;
        margin: 8px 6px 0 10px;
        line-height: 20px;
        font-size: 15px;
        color: #969696!important;
    }
    nav a.sign-up{
        float: right;
        width: 80px;
        height: 36px;
        margin: 8px 6px 0 10px;
        line-height: 20px;
        font-size: 15px;
        border: 1px solid rgba(236,97,73,.7);
        border-radius: 20px;
        color: #ea6f5a!important;
        padding: 6px 12px;
        box-shadow: none;
    }
    nav a.sign-up:hover{
        background-color: rgb(254,247,246);
    }
    nav .user{
        float: right;
        position: relative;
    }
    nav .user:hover{
        background: #f5f5f5;
    }
    nav .user .avatar{
        width: 40px;
        height: 40px;
        display: block;
        margin: 8px 28px 8px 20px;
        position: relative;
    }
    nav .user .avatar:before{
        content: "";
        position: absolute;
        top: 18px;
        right: -14px;
        border-left: 5px solid transparent;
        border-right: 5px solid transparent;
        border-top: 6px solid #999;
    }
    nav .user .avatar img{
        width: 100%;
        height: 100%;
        border: 1px solid #ccc;
        border-radius: 50%;
    }
    nav .user .drop-menu{
        position: absolute;
        left: 0;
        min-width: 160px;
        box-shadow: 0 0 8px rgba(0,0,0,.1);
        font-size: 14px;
        z-index: 5454545;
        background-color: #fff;
    }
    nav .user .drop-menu ul{
        border: 1px solid #f1f1f1;
        padding: 10px 0;
        margin: 0;
    }
    nav .user .drop-menu ul li a{
        padding: 10px;
        display: block;
    }
    nav .user .drop-menu ul li a:hover{
        background-color: #f5f5f5;
    }
    nav .user .drop-menu ul li i{
        margin-right: 15px;
        color: #ea6f5a;
        font-size: 18px;
        margin-left: 10px;
    }
    nav .nav-list{
        overflow: hidden;
        zoom: 1;
    }
    nav .nav-list .nav-list-li{
        float: left;
        margin-right: 15px;
        font-size: 17px;
    }
    nav .nav-list li:nth-of-type(2):hover{
        background-color: #f5f5f5;
    }
    nav .nav-list li:nth-of-type(3):hover{
        background-color: #f5f5f5;
    }
    nav .nav-list li>a{
        display: block;
        height: 55px;
        padding: 15px;
        font-size: 17px;
    }
    nav .nav-list li a .nav-list-i{
        margin-right: 10px;
        font-size: 20px;
    }
    nav .nav-list .active{
        color: #ea6f5a;
    }
    nav .nav-list li:nth-of-type(3){
        /*position: relative;*/
    }
    nav .my-container .drop-menu{
        position: absolute;
        min-width: 200px;
        box-shadow: 0 0 8px rgba(0,0,0,.1);
        z-index: 5454545;
        background-color: #fff;
    }
    nav .my-container .drop-menu ul{
        border: 1px solid #f1f1f1;
        padding: 10px 0;
        margin: 0;
    }
    nav .my-container .drop-menu ul li{
        padding: 0 10px 0 0;
        display: block;
    }
    nav .my-container .drop-menu ul li:hover{
        background-color: #f5f5f5;
    }
    nav .my-container .drop-menu ul li .messageshow-span{
        font-size: 14px;
    }
    nav .my-container .drop-menu ul li i{
        margin-right: 15px;
        color: #ea6f5a;
        font-size: 18px;
        margin-left: 10px;
    }
    nav .nav-list .search{
        padding-left: 15px;
    }
    nav .nav-list .search:hover{

    }
    nav .nav-list .search form{
        margin-top: 9px;
        position: relative;
    }
    nav .nav-list .search form input{
        width: 240px;
        height: 38px;
        border: none;
        background-color: #f1f1f1;
        border-radius: 20px;
        padding: 0 40px 0 20px;
        font-size: 15px;
        transition: width .5s ease-in;
    }
    nav .nav-list .search form input:focus{
        width: 320px;
    }
    nav .nav-list .search form a.search-btn{
        display: block;
        width: 35px;
        height: 35px;
        position: absolute;
        top: 0;
        right: 0;
    }
    nav .nav-list .search form a.active{
        background-color: #969696;
        border-radius: 50%;
        color: #fff!important;
    }
    nav .nav-list .search form i{
        position: absolute;
        top: 10px;
        right: 10px;
    }
    @media (max-width: 1440px) {
        nav .nav-list li a .nav-list-i{
            display: none;
        }
        nav .nav-list .search form input{
            width: 160px;
        }
        nav .nav-list .search form input:focus{
            width: 240px;
        }
    }
    @media (max-width: 1080px) {
        nav .nav-list li a .nav-list-i{
            display: block;
            margin: 0;
        }
        nav .nav-list li a .nav-list-span{
            display: none;
        }
        nav .nav-list .search form input{
            width: 150px;
        }
        nav .nav-list .search form input:focus{
            width: 150px;
        }
    }
    @media (max-width: 822px) {
        nav .nav-list{
            display: none;
        }
    }
</style>