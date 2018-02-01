<template>
    <div>
        <my-header></my-header>
        <div class="index my-container">
            <div class="row">
                <div class="col-8 main">
                    <img class="tag-banner" src="../assets/img/thirty-hot-title.png" alt="">
                    <!--文章列表-->
                    <div class="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/thirty-hot-collection1.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="" class="avatar">
                                            <img src="../assets/img/thirty-hot-avatar1.jpg" alt="">

                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">
                                                MY麦子
                                            </nuxt-link>
                                            <span class="time">2017.12.28 08:16</span>
                                        </div>
                                    </div>
                                    <nuxt-link to="/p/123" class="title">
                                        今年读的这8本书，彻底改变了我
                                    </nuxt-link>
                                    <p class="abstract">

                                        文 | MY麦子 今年三月份的时候辞去了工作，打算好好的放松一下再重新开始，上班的时候就是每天按时去上班，突然不上班了空闲时间也多了起来。平时除了去学车，其他时间都是一个人，...

                                    </p>
                                    <div class="meta">
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