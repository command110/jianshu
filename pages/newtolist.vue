<template>
    <div>
        <my-header></my-header>
        <div class="index my-container">
            <div class="row">
                <div class="col-8 main">
                    <img class="tag-banner" src="../assets/img/new-hot-title.png" alt="">
                    <!--文章列表-->
                    <div class="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/new-hot-collection1.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="" class="avatar">
                                            <img src="../assets/img/new-hot-avatar1.jpg" alt="">

                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">
                                                棋子coffee
                                            </nuxt-link>
                                            <span class="time">昨天 22:21</span>
                                        </div>
                                    </div>
                                    <nuxt-link to="/p/123" class="title">
                                        二胎，一家人的兵荒马乱
                                    </nuxt-link>
                                    <p class="abstract">

                                        （1） 今天的雪很大，大地仿佛一夜间变成一片银装素裹的世界。雪一直在下，越下越大，让大地，房屋建筑，大街小巷都变成了一篇白色的海洋。涓涓坐在开往兰州方向去列车上，看着窗外沿途...

                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            散文随笔
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-eye"></i>579
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>546
                                        </span>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-4 aside">
                    <recommended-author></recommended-author>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from '../components/myHeader'
    import Nuxt from "../.nuxt/components/nuxt";
    import recommendedAuthor from '../components/recommendedAuthor'
    export default {
        components:{
            myHeader,
            Nuxt,
            recommendedAuthor
        }
    }
</script>