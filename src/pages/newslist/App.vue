<template>
    <div id="app">
        <HelloTop/>
        <background/>
        <div class="container">
            <div class="con_content">
                <div class="about_box">
                    <h2 class="nh1"><span>您现在的位置是：<a href="/" target="_blank">网站首页</a>&gt;&gt;<a href="#" target="_blank">个人日记</a></span><b>个人日记</b></h2>
                    <ul class="dtxw box">
                        <li>
                            <div class="dttext f_l">
                                <div>
                                    <h2><a href="/">个人博客模板古典系列之——江南墨卷</a></h2>
                                    <p>个人博客模板古典系列之——江南墨卷个人博客模板古典系列之——江南墨卷个人博客模板古典系列之——江南墨卷原汁原味重现经典....</p>
                                    <span>2017-3-10</span>
                                </div>
                            </div>
                            <div class="xwpic f_r"><a href="/"><img src="./../../assets/images/02.jpg"></a></div>
                        </li>

                        <li>
                            <div class="dttext f_l">
                                <div>
                                    <h2><a href="/">个人博客模板古典系列之——江南墨卷</a></h2>
                                    <p>个人博客模板古典系列之——江南墨卷个人博客模板古典系列之——江南墨卷个人博客模板古典系列之——江南墨卷原汁原味重现经典</p>
                                    <span>2017-3-10</span>
                                </div>
                            </div>
                            <div class="xwpic f_r"><a href="/"><img src="./../../assets/images/02.jpg"></a></div>
                        </li>
                    </ul>
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
export default{
    components:{
        HelloTop,
        background,
        HelloFooter
    }
}
</script>
<style scope>
@import './../../assets/css/base.css';

.dtxw {
    overflow: hidden;
    margin: 30px auto;
}
.dtxw li {
    width: 100%;
    position: relative;
    clear: both;
    list-style: none;
    margin-bottom: 30px;
    overflow: hidden;
}
.dttext {
    line-height: 24px;
}
.dttext {
    width: 60%;
    border-bottom: #838484 1px solid;
    margin-left: 40px;
}
.dttext > div {
    padding: 20px 20px 20px 80px;
}
.dttext h2 {
    font-size: 18px;
    font-weight: normal;
    padding: 5px 10px;
    color: #333;
    background: #ccc;
    margin-bottom: 10px;
}
.dttext span {
    text-align: right;
    float: right;
    color: #999;
}
.xwpic {
    width: 28%;
    overflow: hidden;
    background: #ccc;
}
.xwpic img {
    -webkit-transition: all 0.5s;
    -moz-transition: all 0.5s;
    -o-transition: all 0.5s;
    height: 140px;
    margin: auto;
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
.dtxw li:first-child::before {
    content: "01";
    position: absolute;
    left: 40px;
    top: 40px;
    font-size: 40px;
    color: #aeaeae
}
.dtxw li:nth-child(2)::before {
    content: "02";
    position: absolute;
    left: 40px;
    top: 40px;
    font-size: 40px;
    color: #aeaeae
}
.dtxw li:nth-child(3)::before {
    content: "03";
    position: absolute;
    left: 40px;
    top: 40px;
    font-size: 40px;
    color: #aeaeae
}
.dtxw li:nth-child(4)::before {
    content: "04";
    position: absolute;
    left: 40px;
    top: 40px;
    font-size: 40px;
    color: #aeaeae
}
.dtxw li:nth-child(5)::before {
    content: "05";
    position: absolute;
    left: 40px;
    top: 40px;
    font-size: 40px;
    color: #aeaeae
}
.dtxw li:nth-child(6)::before {
    content: "06";
    position: absolute;
    left: 40px;
    top: 40px;
    font-size: 40px;
    color: #aeaeae
}
</style>