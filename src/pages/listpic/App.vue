<template>
    <div id="app">
        <background/>
        <HelloTop/>
        <div class="container">
            <div class="con_content">
                <div class="about_box">
                    <h2 class="nh1"><span>您现在的位置是：<a href="/" target="_blank">网站首页</a>&gt;&gt;<a href="#" target="_blank">个人相册</a></span><b>个人相册</b></h2>
                    <div class="lispic">
                        <ul>
                            <li><a href="/"><img src="./../../assets/images/01.jpg"><span>图片展示</span></a></li>
                            <li><a href="/"><img src="./../../assets/images/02.jpg"><span>图片展示</span></a></li>
                            <li><a href="/"><img src="./../../assets/images/03.jpg"><span>图片展示</span></a></li>
                            <li><a href="/"><img src="./../../assets/images/04.jpg"><span>图片展示</span></a></li>
                            <li><a href="/"><img src="./../../assets/images/03.jpg"><span>图片展示</span></a></li>
                            <li><a href="/"><img src="./../../assets/images/06.jpg"><span>图片展示</span></a></li>
                            <li><a href="/"><img src="./../../assets/images/01.jpg"><span>图片展示</span></a></li>
                            <li><a href="/"><img src="./../../assets/images/02.jpg"><span>图片展示</span></a></li>
                        </ul>
                    </div>
                    <div class="pagelist">页次：1/1 每页25 总数10<a href="/">首页</a><a href="/">上一页</a><a href="/">下一页</a><a href="/">尾页</a></div>
                </div>
            </div>
            <div class="blank"></div>
        </div>
        <HelloFooter/>
    </div>

</template>
<script>
import HelloTop from "./../../components/HelloTop";
import background from "./../../components/background";
import HelloFooter from "./../../components/HelloFooter";
export default {
    components:{
        HelloTop,
        background,
        HelloFooter
    }
}

</script>
<style scope>
@import './../../assets/css/base.css';


.lispic {
    padding: 20px 0;
    overflow: hidden;
}
.lispic li {
    float: left;
    text-align: center;
    width: 200px;
    border: #ccc 5px solid;
    overflow: hidden;
    background: #ccc;
    margin: 10px 10px 10px 9px;
    position: relative;
}
.lispic li img {
    display: block;
    margin: auto;
    height: 160px;
    width: auto;
    -webkit-transition: all 0.5s;
    -moz-transition: all 0.5s;
    -o-transition: all 0.5s;
}
.lispic li span {
    padding: 10px 0;
    display: block;
    position: absolute;
    overflow: hidden;
    text-align: center;
    bottom: 0;
    background: rgba(0, 0, 0, 0.55);
    width: 100%;
    color: #fff;
}
.pagelist {
    text-align: center;
    color: #666;
    width: 100%;
    clear: both;
    margin: 10px 0;
    display: block;
}
.pagelist a {
    color: #666;
    margin: 0 2px;
}

.blank {
    height: 8px;
    overflow: hidden;
    width: 100%;
    margin: auto;
    clear: both;
}
</style>