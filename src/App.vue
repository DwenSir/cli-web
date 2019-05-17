<template>
  <div id="app" :style="{height:app.height}">
    <!--左右结构 伸缩布局-->
    <div class="box_nav">
      <div class="logo_name"><img :src="initConf.img_addr" alt="tools img"><span v-text="initConf.tools_name"></span></div>
      <div class="nav_content">
        <el-row class="tac">
          <el-col :span="12">
            <el-menu router :default-active="$route.path" class="el-menu-vertical-demo" background-color="#202d40" text-color="#fff" active-text-color="#ffd04b">
              <el-submenu v-for="(v, i) in initConf.class_arr" :key="i" :index="v.index">
                <template slot="title">
                  <i class="el-icon-link"></i>
                  <span v-text="v.name"></span>
                </template>
                <el-menu-item v-for="sele in v.pages" v-text="sele.name" :index="sele.route"></el-menu-item>
              </el-submenu>
            </el-menu>
          </el-col>
        </el-row>
      </div>
    </div>
    <div class="box_view">
      <router-view />
    </div>
  </div>
</template>

<script>
  // 导入配置文件
  import conf from '../public/config/init'
    export default {
        name: 'app',
        data(){
            return{
                app:{
                    height:0,
                },
                isCollapse: true,
                initConf:conf,
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
            },
            handleOpen() {

            },
            handleClose() {

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
  /* 这个属性保证导航栏不会宽度和边框不会出现白边*/
  .el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    border: 0;
  }
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
    .logo_name{
      text-align: center;
      margin: 16px 0;
      img{
        border-radius: 50%;
        border: 2px solid #fff;
        height: 50px;
        width: 50px;
        margin: 0 10px;
      }
    }
    .nav_content{

    }
  }
  .box_view{
    .xflex(9);
  }

}
</style>
