<template>
    <div>
        <div class="comment-list" id="comment-list">
            <!--提交的留言表单-->
            <form class="new-comment">
                <nuxt-link to="/u/123" class="avatar">
                    <img src="../assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <textarea @focus="send_one = true" placeholder="写下你的评论">

                </textarea>
                <transition :duration="500" name="fade">
                <div v-if="send_one" class="write-function-block clearfix">
                    <div class="emoji-modal-wrap">
                        <a @click="showEmoji = ! showEmoji" href="javascript:void (0)" class="emoji">
                            <i class="fa fa-smile-o"></i>
                        </a>
                        <transition :duration="500" name="fade">
                        <div v-if="showEmoji" class="emoji-modal arrow-up"></div>
                        </transition>
                    </div>
                    <div class="hint">
                        Ctrl+Enter发送
                    </div>
                    <a class="btn btn-send" href="javascript:void (0)">发送</a>
                    <a @click="send_one = false" class="cancel" href="javascript:void (0)">取消</a>
                </div>
                </transition>
            </form>
        </div>
    </div>
</template>
<script>
    export default {
        name:'myComment',
        data(){
            return{
                send_one:false,
                senf_two:false,
                showEmoji:false,
                showOther:false
            }
        },
        methods:{
            showEmoji:function () {

            }
        }
    }
</script>
<style>
    .fade-enter-active,.fade-leave-active {
        opacity: 1;
        transition: .3s;
        -webkit-transition: .3s
    }
    .fade-enter,.fade-leave-to {
        opacity: 0;
        transform: translate3d(0,-5%,0);
        -webkit-transform: translate3d(0,-5%,0);
        transition: .3s;
        -webkit-transition: .3s
    }
    .note .post .comment-list{
        padding-top: 20px;
        margin-bottom: 200px;/*yihuishanni*/
    }
    .note .post .comment-list .new-comment {
        position: relative;
        margin: 0 0 20px 48px;
    }
    .note .post .comment-list .avatar{
        width: 38px;
        height: 38px;
        display: inline-block;
        margin-right: 5px;
    }
    .note .post .comment-list .new-comment .avatar{
        position: absolute;
        left: -48px;
    }
    .note .post .comment-list .new-comment textarea{
        padding: 10px 15px;
        width: 100%;
        height: 80px;
        font-size: 13px;
        border: 1px solid #dcdcdc;
        border-radius: 4px;
        background-color: hsla(0,0%,71%,.1);
        resize: none;
        display: inline-block;
        vertical-align: top;
        outline-style: none;
    }
    .note .post .comment-list .new-comment .meoji-modal-warp{
        position: relative;
    }
    .note .post .comment-list .new-comment .emoji {
        float: left;
        margin-top: 14px;
    }
    .note .post .comment-list .new-comment .emoji i{
        font-size: 25px;
        color: #969696;
    }
    .note .post .comment-list .new-comment .emoji i:hover{
        color: #333;
    }
    .note .post .comment-list .new-comment .hint {
        float: left;
        margin: 20px 0 0 20px;
        font-size: 13px;
        color: #969696;
    }
    .note .post .comment-list .new-comment .cancel {
        float: right;
        font-size: 16px;
        margin: 18px 30px 0 0;
        color: #969696!important;
    }
    .note .post .comment-list .new-comment .cancel:hover{
        color: #333!important;
    }
    .note .post .comment-list .new-comment .btn-send{
        float: right;
        width: 78px;
        margin: 10px 0;
        padding: 8px 18px;
        font-size: 18px;
        border-radius: 20px;
        background: #42c02e;
        color: #fff!important;
        outline: none;
        box-shadow: none;
    }
    .note .post .comment-list .new-comment .btn-send:hover{
        background: #3db922;
    }
    .note .post .comment-list .new-comment .emoji-modal-wrap .emoji-modal{
        position: absolute;
        top: 130px;
        left: -48px;
        width: 360px;
        height: 100px;
        border: 1px solid #d9d9d9;
        background-color: #ffffff;
        border-radius: 4px;
        z-index: 4545454545;
    }
    .arrow-up:after{
        content: "";
        display: inline-block;
        width: 15px;
        height: 15px;
        position: absolute;
        background: #fff;
        top: -1px;
        left: 48px;
        border-left: 1px solid #d9d9d9;
        border-top: 1px solid #d9d9d9;
        transform: translate3d(0,-50%,0)rotate(45deg);
    }
</style>