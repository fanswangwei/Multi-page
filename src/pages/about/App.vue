<template>
    <div id="app">
        <background/>
        <hello-top/>
        <div class="jztop"></div>
        <div class="container">
            <div class="con_content">
                <div class="about_box">
                    <h2 class="nh1"><span>您现在的位置是：<a href="/" target="_blank">网站首页</a>&gt;&gt;<a href="#" target="_blank">信息浏览</a></span><b>个人简介</b></h2>
                    <div class="f_box">
                        <p class="a_title">个人简介</p>
                        <p class="p_title"></p>
                    </div>
                    <ul class="about_content">
                        <p> 人生就是一个得与失的过程，而我却是一个幸运者，得到的永远比失去的多。生活的压力迫使我放弃了轻松的前台接待，放弃了体面的编辑，换来虽有些蓬头垢面的工作，但是我仍然很享受那些熬得只剩下黑眼圈的日子，因为我在学习使用Photoshop、Flash、Dreamweaver、ASP、PHP、JSP...中激发了兴趣，然后越走越远....</p>
                        <p><img src="./../../assets/images/01.jpg"></p>
                        <p>“冥冥中该来则来，无处可逃”。 </p>
                    </ul>
                </div>
                <div class="blank"></div>
            </div>
        </div>
        <hello-footer/>
    </div>
</template>

<script>
import HelloTop from './../../components/HelloTop'
import background from './../../components/background'
import HelloFooter from './../../components/HelloFooter'

export default {
    components: {
        HelloTop,
        background,
        HelloFooter
    }
}
</script>

<style scope>
@import "./../../assets/css/base.css";

.p_title {
    text-align: center;
    font-size: 20px;
    color: #333;
    line-height: 50px;
}
.a_title {
    text-align: center;
    font-size: 24px;
    font-weight: bold;
    color: #000;
    line-height: 50px;
}
.about_content {
    line-height: 24px;
    font-size: 14px;
    padding: 20px;
}
.about_content p {
    margin-bottom: 15px;
    text-indent: 2em;
}
.about_content p img {
    margin: auto;
}
.blank {
    height: 8px;
    overflow: hidden;
    width: 100%;
    margin: auto;
    clear: both;
}
</style>
