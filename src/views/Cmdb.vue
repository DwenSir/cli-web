<template>
    <div id="cmdb">
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
        homeazzzzzzzzzzzzzzzzzzzzzzzzz
    </div>
</template>

<script>
    export default {
        name: "cmdb"
    }
</script>

<style scoped lang="less">
    /*start less类*/
    .xflex(@num){
        flex: @num;
        -webkit-flex: @num;
        -ms-flex: @num;
        -moz-box-flex: @num;
    }
    .xdisplayflex(){
        display: -webkit-box;
        display: -webkit-flex;
        display: -ms-flexbox;
        display: flex
    }
    .xboxshow(){
        -moz-box-shadow:1px 1px 5px #515151;
        -webkit-box-shadow:1px 1px 5px #515151;
        box-shadow:1px 1px 5px #515151;
    }
    .bgimg(@path){
        background-image: url(@path);
        -moz-background-size:cover; /* 老版本的 Firefox */
        background-repeat:no-repeat;
        background-size: cover;
        background-position: center center;
    }
    @bgcolor: #202d40;
    /*end less类*/
    #cmdb{
        color: @bgcolor;
    }
</style>