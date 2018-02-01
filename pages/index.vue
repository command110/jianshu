<template>
    <div>
        <my-header></my-header>
        <div class="index my-container">
            <div class="row">
                <!--首页左侧-->
                <div class="col-8 main">
                    <!--首页左侧轮播图-->
                    <div class="banner">
                        <b-carousel id="carousel1"
                                    controls
                                    indicators
                                    background="#ababab"
                                    :interval="4000"
                                    v-model="slide"
                                    @sliding-start="onSlideStart"
                                    @sliding-end="onSlideEnd"
                        >
                            <!-- Text slides with image -->
                            <b-carousel-slide>
                                <img slot="img" class="d-block img-fluid w-100"
                                     src="../assets/img/banner1.jpg" alt="image slot">
                            </b-carousel-slide>

                            <!-- Slides with custom text -->
                            <b-carousel-slide>
                                <img slot="img" class="d-block img-fluid w-100"
                                     src="../assets/img/banner2.jpg" alt="image slot">
                            </b-carousel-slide>

                            <!-- Slides with image only -->
                            <b-carousel-slide>
                                <img slot="img" class="d-block img-fluid w-100"
                                     src="../assets/img/banner3.jpg" alt="image slot">
                            </b-carousel-slide>

                            <!-- Slides with img slot -->
                            <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
                            <b-carousel-slide>
                                <img slot="img" class="d-block img-fluid w-100"
                                     src="../assets/img/banner4.jpg" alt="image slot">
                            </b-carousel-slide>

                            <!-- Slide with blank fluid image to maintain slide aspect ratio -->
                            <b-carousel-slide>
                                <img slot="img" class="d-block img-fluid w-100"
                                     src="../assets/img/banner5.jpg" alt="image slot">
                            </b-carousel-slide>
                            <b-carousel-slide>
                                <img slot="img" class="d-block img-fluid w-100"
                                     src="../assets/img/banner6.jpg" alt="image slot">
                            </b-carousel-slide>
                        </b-carousel>
                    </div>
                    <!--首页左侧推荐专题-->
                    <div class="recommend-collection">
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection1.png" alt="">
                            <span>旅行·在路上</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection2.jpg" alt="">
                            <span>故事</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg" alt="">
                            <span>人文社科</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg" alt="">
                            <span>读书</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg" alt="">
                            <span>社会热点</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg" alt="">
                            <span>手绘</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg" alt="">
                            <span>IT·互联网</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123" class="more-collection">
                            等多热门专题
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                    <!--首页左侧推荐专题下线-->
                    <div class="split-line"></div>
                    <!--文章列表-->
                    <div class="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic2.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">

                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link to="/p/123" class="title">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
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
                            <li>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">

                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link to="/p/123" class="title">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
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
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic2.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">

                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link to="/p/123" class="title">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
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
                            <li>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">

                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link to="/p/123" class="title">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
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
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic2.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">

                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link to="/p/123" class="title">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
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
                            <li>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">

                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link to="/p/123" class="title">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短片小说
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
                    <!--阅读更多-->
                    <nuxt-link to="/" class="load-more">
                        阅读更多
                    </nuxt-link>
                </div>
                <!--首页右侧-->
                <div class="col-4 aside">
                    <!--首页右侧图片列表-->
                    <div class="board">
                        <nuxt-link to="/newtolist">
                            <img src="../assets/img/1.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/hotseven">
                            <img src="../assets/img/2.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/hotthirty">
                            <img src="../assets/img/3.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/4.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/5.png" alt="">
                        </nuxt-link>
                        <transition>
                        <div class="ma-download" v-show="maShow">
                            <img src="../assets/img/download.png" alt="">
                            <div class="ma-triangle"></div>
                        </div>
                        </transition>

                    </div>
                    <!--首页右侧APP下载二维码-->
                    <div class="app-download" @mouseover="maShow=true" @mouseleave="maShow=false">
                        <nuxt-link to="/download">
                            <img src="../assets/img/download.png" alt="">
                            <div class="info">
                                <div class="title">下载简书手机App <i class="fa fa-angle-right" aria-hidden="true"></i></div>
                                <div class="description">随时随地发现和创作内容</div>
                            </div>
                        </nuxt-link>
                    </div>
                    <recommended-author></recommended-author>
                </div>
            </div>
        </div>
        <footer>
            <div class="my-container">
                <div class="row">
                    <div class="col-8">
                        <nuxt-link class="a-footer" to="/">关于简书</nuxt-link><em>·</em>
                        <nuxt-link class="a-footer" to="/">联系我们</nuxt-link><em>·</em>
                        <nuxt-link class="a-footer" to="/">加入我们</nuxt-link><em>·</em>
                        <nuxt-link class="a-footer" to="/">简书出版</nuxt-link><em>·</em>
                        <nuxt-link class="a-footer" to="/">品牌与徽章</nuxt-link><em>·</em>
                        <nuxt-link class="a-footer" to="/">帮助中心</nuxt-link><em>·</em>
                        <nuxt-link class="a-footer" to="/">合作伙伴</nuxt-link>
                        <div class="icp">
                            ©2012-2018 上海佰集信息科技有限公司 / 简书 / 沪ICP备11018329号-5 /
                            <nuxt-link to="/">
                                <img src="" alt="">
                            </nuxt-link>
                            <nuxt-link to="/">
                                沪公网安备31010402002252号 /
                            </nuxt-link>
                            <nuxt-link to="/">
                                <img src="" alt="">
                            </nuxt-link>
                            举报电话：021-34770013 /
                            <nuxt-link to="/">
                                <img src="" alt="">
                            </nuxt-link>
                        </div>
                    </div>
                </div>
            </div>
        </footer>
    </div>
</template>
<script>
    import myHeader from '../components/myHeader'
    import Nuxt from "../.nuxt/components/nuxt";
    import recommendedAuthor from '../components/recommendedAuthor'
    export default {
        data () {
            return {
                slide: 0,
                sliding: null,
                maShow:false
            }
        },
        components:{
            Nuxt,
            myHeader,
            recommendedAuthor
        },
        methods: {
            onSlideStart (slide) {
                this.sliding = true
            },
            onSlideEnd (slide) {
                this.sliding = false
            }
        }
    }
</script>