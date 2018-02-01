<template>
    <div>
        <my-header></my-header>
        <div class="index my-container">
            <div class="row">
                <div class="col-8 main">
                    <img class="tag-banner" src="../assets/img/seven-hot-title.png" alt="">
                    <!--文章列表-->
                    <div class="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/seven-hot-collection1.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="" class="avatar">
                                            <img src="../assets/img/seven-hot-avatar1.png" alt="">

                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">
                                                七小葩
                                            </nuxt-link>
                                            <span class="time">01.23 07:42</span>
                                        </div>
                                    </div>
                                    <nuxt-link to="/p/123" class="title">
                                        这15个图片网站，至少让你的效率翻一倍！
                                    </nuxt-link>
                                    <p class="abstract">

                                        如果你还在用百度搜图，那真是“棒棒哒”，像你这么专一的人不多了。 经常有人会问我，你一般在哪找的图片？ 不少朋友都会有自己的素材库，需要时提取就可以了。 不过像我这么懒的人，...

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