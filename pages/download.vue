<template>
    <div>
        <my-header></my-header>
        <div class="container-fluid">
            <div class="row">
                <div class="my-container top-part">
                    <div class="top-logo">
                        <img src="../assets/img/misc-logo.png" alt="">
                        <div class="info">
                            <div class="title">创作你的创作</div>
                            <div class="slogan">一个优质创作社区</div>
                        </div>
                    </div>
                    <img class="background" src="../assets/img/misc-background.png" alt="">
                    <img class="phone-img" src="../assets/img/misc-phone.png" alt="">
                    <div class="top-qrcode">
                        <img src="../assets/img/download-apps-page-top-qrcode.png" alt="">
                        <div class="title">扫码下载简书App</div>
                        <div class="description">随时随地发现和创作内容</div>
                    </div>
                </div>
                <div class="row-first"></div>
            </div>
            <div class="row">
                <div class="my-container middle-part">
                    <div class="text-block">
                        <h3>轻松创作精美图文</h3>
                        <h6>简单优雅的设计，可以一次上传多张图片、实时保存、多端同步，使创作分享更方便快捷</h6>
                    </div>
                    <div class="col-xs-24">
                        <img class="pic1" src="../assets/img/misc-pic1.png" alt="">
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="my-container middle-part">
                    <div class="col-left">
                        <img class="pic-left" src="../assets/img/misc-pic2.png" alt="">
                    </div>
                    <div class="text-block text-block-left">
                        <h3>多元化的创作社区</h3>
                        <h6>一篇短文、一首诗、一幅画，在这里，你的创作将得到全世界的赞赏</h6>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="my-container middle-part">
                    <div class="text-block text-block-right">
                        <h3>百万创作者在简书相遇</h3>
                        <h6>在简书，仍有数百万创作者在坚持产出优质创作，有数千万读者在用心交流创作；众多精彩创作，只在简书看得到</h6>
                    </div>
                    <div class="col-right">
                        <img class="pic-right" src="../assets/img/misc-pic3.png" alt="">
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="my-container middle-part">
                    <div class="col-left">
                        <img class="pic-left" src="../assets/img/misc-pic4.png" alt="">
                    </div>
                    <div class="text-block text-block-left">
                        <h3>自由地交流和沟通</h3>
                        <h6>你可以发表评论、沟通想法。觉得不够？还能给创作者发简信，和无数传遍中文互联网的创作者直接交流</h6>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="bottom-part">
                    <img class="qrcode" src="../assets/img/download-apps-page-top-qrcode.png" alt="">
                    <img class="background" src="../assets/img/misc-background.png" alt="">
                    <div>扫码下载简书App</div>
                    <div class="bottom-logo">
                        <img src="../assets/img/misc-logo.png" alt="">
                        <div class="info">
                            <div class="title">创作你的创作</div>
                            <div class="slogan">一个优质创作社区</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from '../components/myHeader'
    import Nuxt from "../.nuxt/components/nuxt";
    export default {
        components:{
            myHeader,
            Nuxt
        }
    }
</script>