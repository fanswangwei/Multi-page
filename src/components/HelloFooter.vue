<template>
    <div class="">
        <footer>
            <div class="footer">
                <div class="f_l">
                    <p>All Rights Reserved 版权所有：<a href="/">个人博客</a> 备案号：蜀ICP备00000000号</p>
                </div>
                <div class="f_r textr">
                    <p>Design by BratsWang</p>
                </div>
            </div>
        </footer>
    </div>
</template>

<script>


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
footer {
    background: url('./../assets/images/footerbg.png') repeat-x;
    padding: 20px 0;
    color: #ccc;
    margin: 20px 0 0 0;
}
.footer {
    width: 1000px;
    margin: auto;
    overflow: hidden;
}
.f_l {
    float: left;
}
.f_r {
    float: right;
}
.textr {
    text-align: right;
}
.footer p {
    line-height: 24px;
}
.footer a {
    color: #ccc;
}
</style>
