<template>
  <div id="app" :style="{height:app.height}">
    <!--左右结构 伸缩布局-->
    <div class="box_nav">
      <div class="img_name">
        <div class="tools_img">
          <!--<img src="../public/img/img.jpg" alt="tools img">-->
        </div>
        <div class="tools_name">simple</div>
      </div>
      <div class="nav_content">

      </div>
    </div>
    <div class="box_view">
      <!--<router-view />-->
    </div>
  </div>
</template>

<script>
    export default {
        name: 'app',
        data(){
            return{
                app:{
                    height:0,
                }
            }
        },
        mounted(){
            this.getHeight();
        },
        methods:{
            getHeight(){
                // 获取屏幕真实高度
                const H = window.innerHeight || document.documentElement.clientHeight || document.body.clientHeight;
                this.app.height = H + "px"
            }
        }
    }
</script>

<style lang="less">
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
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
  overflow: hidden;
  .xdisplayflex();
  .box_nav{
    .xflex(1);
    background-color: @bgcolor;
    .img_name{
      .xdisplayflex();
      height: 50px;
      .tools_img{
        .xflex(3);
        margin: 10px 5px;
        img{
          height: 100%;
          width: 100%;
        }
      }
      .tools_name{
        .xflex(7);
        margin: 10px 20px;
      }
    }

  }
  .box_view{
    .xflex(9);
  }

}
</style>
