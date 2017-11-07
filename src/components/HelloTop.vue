<template>
    <div class="top">
        <header>
            <div class="headtop"></div>
            <div class="contenttop">
                <div class="logo f_l">在这儿遇到你，是我一生最美的旅行</div>
                <div class="search f_r">
                    <form action="/e/search/index.php" method="post" name="searchform" id="searchform">
                        <input name="keyboard" id="keyboard" class="input_text" value="请输入关键字" style="color: rgb(153, 153, 153);" onfocus="if(value=='请输入关键字'){this.style.color='#000';value=''}" onblur="if(value==''){this.style.color='#999';value='请输入关键字'}" type="text">
                        <input name="show" value="title" type="hidden">
                        <input name="tempid" value="1" type="hidden">
                        <input name="tbname" value="news" type="hidden">
                        <input name="Submit" class="input_submit" value="搜索" type="submit">
                    </form>
                </div>
                <div class="blank"></div>
                <nav>
                    <div class="navigation">
                        <ul class="menu">
                            <li><a href="index.html">首页</a></li>
                            <li v-on:mouseenter="hoverEnter('about')" v-on:mouseleave="hoverleave('about')">
                                <a href="#">关于我</a>
                                <ul v-show="showHide.about">
                                    <li><a href="about.html">个人简介</a></li>
                                    <li><a href="listpic.html">个人相册</a></li>
                                </ul>
                            </li>
                            <li v-on:mouseenter="hoverEnter('diary')" v-on:mouseleave="hoverleave('diary')">
                                <a href="#">我的日记</a>
                                <ul v-show="showHide.myDiary">
                                    <li><a href="newslist.html">个人日记</a></li>
                                    <li><a href="newslist.html">学习笔记</a></li>
                                </ul>
                            </li>
                            <li><a href="newslist.html">技术文章</a> </li>
                            <li><a href="#">给我留言</a> </li>
                        </ul>
                    </div>
                </nav>
            </div>
        </header>
    </div>
</template>

<script>
export default{
    data(){
        return{
            showHide: {
                about: false,
                myDiary: false
            }

        }
    },
    methods: {
        hoverleave(status){
            if(status == 'about'){
                this.showHide.about = false;
            }else if(status == 'diary'){
                this.showHide.myDiary = false;
            }
        },
        hoverEnter(status){
            if(status == 'about'){
                this.showHide.about = true;
            }else if(status == 'diary'){
                this.showHide.myDiary = true;
            }
        }
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* 共用css */
* {
    margin: 0;
    padding: 0
}
img {
    border: 0;
    display: block
}
ul, ol, li {
    list-style: none;
}
h1, h2, h3, h4, h5, h6 {
    font-size: 100%;
    font-weight: normal;
}
a {
    outline: none;
}
/*默认链接颜色 */
a:link, a:visited, a:active {
    text-decoration: none;
    color: #000000
}
a:hover {
    text-decoration: none;
    color: #000;
}
.clear {
    clear: both;
}
.blank {
    height: 8px;
    overflow: hidden;
    width: 100%;
    margin: auto;
    clear: both
}
.f_l {
    float: left
}
.f_r {
    float: right
}

header {
    width: 100%;
    
}
.headtop {
    background: url('./../assets/images/topbg.png') repeat-x;
    height: 28px;
}
.contenttop {
    width: 1000px;
    margin: auto;
}
.logo {
    padding: 20px 0 20px 20px;
    font-size: 26px;
    font-family: "微软雅黑", sans-serif;
    color: #333;
    font-weight: bold;
}
/*search*/
.search {
    width: 240px;
    margin: 50px 0 0 0
}
.input_text {
    padding-left: 5px;
    border: 1px solid #ccc;
    width: 158px;
    height: 26px;
    line-height: 26px;
    background-color: #e5e5e5;
}
.input_submit {
    background-color: #333;
    color: #FFF;
    margin-left: 5px;
    width: 50px;
    border: none;
    cursor: pointer;
    height: 28px;
    line-height: 28px;
    border-radius: 5px;
}
/*nav*/
nav {
    margin: 0 0 15px 0
}
.navigation {
    height: 64px;
    background: url('./../assets/images/navbg.png') no-repeat;
    font-family: "微软雅黑";
}
.menu {
    position: relative;
    margin-left: 70px;
    padding-top: 10px
}
.menu li {
    float: left;
    width: 110px;
    text-align: center;
    position: relative;
    line-height: 46px;
}
.menu li a {
    display: block;
    text-decoration: none;
    color: #fff;
    font-size: 15px;
    font-weight: bold
}
.menu ul {
    position: relative;
    background: #333;
    z-index: 300;
}
.menu li ul {
    /* display: none; */
    width: 110px;
    position: absolute;
    TOP: 40px;
    left: 0;
}
.menu li ul li {
    font-size: 12px;
    height: 28px;
    line-height: 28px
}
.menu li ul li a {
    font-size: 14px
}
.menu li ul li a:hover {
    background: #000
}

</style>
