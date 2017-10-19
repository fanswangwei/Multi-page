<template>
    <div id="app">
        <background/>
        <hello-top/>
        <div class="jztop"></div>
        <div class="container">
            <div class="bloglist f_l">
                <div v-for=" item in articleList">
                    <h3><a :title="item.title" :href="item.url" target="_blank">{{item.title}}</a></h3>
                    <figure><img :src="item.images_cover" :alt="item.title"></figure>
                    <ul>
                        <p>{{item.summary}}</p>
                        <a :title="item.title" :href="item.url" target="_blank" class="readmore">阅读全文&gt;&gt;</a>
                    </ul>
                    <p class="dateview">
                        <span>{{item.time}}</span>
                        <span>作者：<a href="about.html" target="_blank">[{{item.author}}]</a></span></p>
                </div>
            </div>
            <div class="r_box f_r">
                <div class="tit01">
                    <h3 class="tit">关注我</h3>
                    <div class="gzwm">
                        <ul>
                            <li><a class="tel" href="#" target="_blank">我的电话</a></li>
                            <li><a class="email" href="#mailto:admin@admin.com" target="_blank">我的邮箱</a></li>
                            <li><a class="qq" href="#" target="_blank">我的QQ</a></li>
                            <li><a class="prize" href="#">个人奖项</a></li>
                        </ul>
                    </div>
                </div>
                <!--tit01 end-->

                <div class="tuwen">
                    <h3 class="tit">图文推荐</h3>
                    <ul>
                        <li v-for="item in imgArticleList">
                            <a :href="item.url" target="_blank"><img :src="item.images_cover"><b>{{item.title}}</b></a>
                            <p>
                                <span class="tulanmu"><a :href="item.url" target="_blank">{{item.fenlei}}</a></span>
                                <span class="tutime">{{item.time}}</span>
                            </p>
                        </li>
                    </ul>
                </div>
                <div class="ph">
                    <h3 class="tit">点击排行</h3>
                    <ul class="rank">
                        <li v-for=" item in articleList">
                            <a :title="item.title" :href="item.url" target="_blank">{{item.title}}</a>
                        </li>
                    </ul>
                </div>
                <div class="ad"> <img src="/static/images/03.jpg"> </div>
            </div>
        </div>
        <hello-footer/>
    </div>
</template>

<script>
import background from './../../components/background'
import HelloTop from './../../components/HelloTop'
import HelloFooter from './../../components/HelloFooter'

export default {
    name: 'app',
    components: {
        background,
        HelloTop,
        HelloFooter
    },
    data(){
        return{
            articleList: [],
            imgArticleList: []
        }
    },
    mounted() {
        this.getArticleList();
        this.getImgArticle();
    },
    methods:{
        getArticleList(){
            this.$http.get('/static/data/articleList.json').then(result => {
                this.articleList = result.body;
            })
        },
        getImgArticle(){
            let params = {
                author: 'Brats Wang',
                fenlei: 'phone'
            }
            this.$http.get('/static/data/imgArticle.json', {param: params}).then( result => {
                this.imgArticleList = result.body;
            })
        }
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
}
a:link, a:visited, a:active {
    text-decoration: none;
    color: #000000;
}
li {
    list-style: none;
    display: list-item;
    text-align: -webkit-match-parent;
}
#app .jztop {
    background: url('/static/images/jztop.png') no-repeat;
    width: 1034px;
    margin: auto;
    height: 32px;
}
#app .container {
    background: rgba(204, 204, 204, 0.3);
    overflow: hidden;
    width: 1000px;
    margin: auto;
    border-left: #d2d2d2 1px solid;
    border-right: #d2d2d2 1px solid;
    border-bottom: #d2d2d2 1px solid;
}
.bloglist {
    width: 620px;
    overflow: hidden;
    margin-left: 20px;
    margin-bottom: 20px;
}
.f_l {
    float: left;
}
.bloglist h3 {
    margin: 20px 0 10px 0;
    color: #333;
    font-size: 16px;
    font-family: "微软雅黑";
}
.bloglist figure {
    float: left;
    width: 25%;
}
.bloglist figure img {
    padding: 4px;
    border: #f4f2f2 1px solid;
    width: 140px;
}
.bloglist ul {
    float: left;
    width: 70%;
    margin: 10px 0px 0 15px;
    line-height: 20px;
}
a.readmore {
    background: #333;
    color: #fff;
    padding: 5px 10px;
    float: right;
    margin: 20px 0 0 0;
}
.dateview {
    width: 100%;
    overflow: hidden;
    clear: both;
    margin: 10px 0 0 0;
    display: inline-block;
    background: #f6f6f6 url('/static/images/time.jpg') 15px center no-repeat;
    line-height: 26px;
    font-size: 13px;
    height: 26px;
    color: #838383;
    padding-left: 25px;
}
.dateview span {
    margin: 0 10px;
}
.dateview span a {
    color: #41607d;
}
.r_box {
    width: 300px;
    margin: 20px 20px 0 0;
}
.f_r {
    float: right;
}
.tit {
    line-height: 44px;
    color: #fff;
    font-size: 18px;
    height: 44px;
    background: url('/static/images/rtitbg.png') no-repeat;
    padding-left: 40px;
    margin: 0 0 10px 0;
}
.gzwm ul {
    width: 100%;
    overflow: hidden;
}
.gzwm li {
    width: 60px;
    margin: 0 10px 0 5px;
    float: left;
}
.gzwm .tel {
    background: url('/static/images/gz01.png') no-repeat;
}
.gzwm li a {
    color: #747F8C;
    width: 62px;
    font-size: 13px;
    text-align: center;
    padding-top: 60px;
    float: left;
}
.gzwm .email {
    background: url('/static/images/gz02.png') no-repeat;
}
.gzwm .qq {
    background: url('/static/images/gz03.png') no-repeat;
}
.gzwm .prize {
    background: url('/static/images/gz04.png') no-repeat;
}
.tuwen {
    width: 100%;
    clear: both;
    overflow: hidden;
    margin: 20px 0;
}
.tuwen li {
    overflow: hidden;
    clear: both;
    margin-bottom: 10px;
}
.tuwen li img {
    width: 70px;
    height: 57px;
    float: left;
    margin-right: 15px;
}
.tuwen li b {
    overflow: hidden;
    width: 100%;
    font-weight: normal;
    color: #333;
    font-size: 14px;
    line-height: 30px;
}
.tuwen p {
    font-size: 13px;
    margin-top: 5px;
}
.tuwen li span {
    color: #999;
    margin-right: 10px;
}
.tulanmu {
    background: url('/static/images/lanmbq.png') no-repeat center left;
    padding-left: 17px;
}
.tutime {
    background: url('/static/images/datepng.png') no-repeat left center;
    padding-left: 15px;
}
.ph {
    overflow: hidden;
}
.rank {
    margin: 10px 0;
}
.rank li {
    height: 25px;
    line-height: 25px;
    clear: both;
    padding-left: 5px;
    overflow: hidden;
    padding-left: 15px;
    background: url('/static/images/libg.jpg') no-repeat left center;
}
.rank li:first-child a {
    color: #f00;
}
.rank li a {
    display: block;
    font-size: 13px;
    height: 25px;
    color: #333;
}
.ad {
    width: 300px;
    overflow: hidden;
    margin: 30px 0;
}
.ad img {
    width: 300px;
}
</style>
