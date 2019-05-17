<template>
    <div id="login">
        <div class="login-info">
            <h3>登陆平台</h3>
            <div class="box-input">
                <!--ip-->
                <i class="el-icon-paperclip"></i><input v-model="loginInfo.ip" type="text" placeholder="请输入连接的ip地址!">
            </div>
            <div class="box-input">
                <!--usename-->
                <i class="el-icon-s-custom"></i><input v-model="loginInfo.usename" type="text" placeholder="请输入用户名!">
            </div>
            <div class="box-input">
                <!--password-->
                <i class="el-icon-lock"></i><input v-model="loginInfo.password" type="password" placeholder="请输入密码!">
            </div>
            <div class="btn">
                <!--button-->
                <el-button type="primary" :loading="loginInfo.signin" :disabled="loginInfo.status">登录</el-button>
                <el-button type="primary" :loading="loginInfo.signout" :disabled="!loginInfo.status">注销</el-button>
                <!--<el-button type="success" icon="el-icon-check" circle></el-button>-->
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Login",
        data(){
            return{
                loginInfo:{
                    ip:"",
                    usename:"",
                    password:"",
                    status:false,
                    signin:false,
                    signout:false,
                }
            }
        }
    }
</script>

<style scoped lang="less">
    /*start less类*/
    .xdisplayflex(){
        display: -webkit-box;
        display: -webkit-flex;
        display: -ms-flexbox;
        display: flex
    }
    .xtransform(@num1, @num2){
        -webkit-transform: translate(@num1, @num2);
        -moz-transform: translate(@num1, @num2);
        -ms-transform: translate(@num1, @num2);
        -o-transform: translate(@num1, @num2);
        transform: translate(@num1, @num2);
    }
    @bgcolor: #202d40;
    /*end less类*/
    #login{
        height: 100%;
        width: 100%;
        /*background-color: rgba(60, 63, 65, 0.3);*/
        background: url("../assets/img/bg2.jpg") no-repeat center;
        position: relative;
        .login-info{
            width: 500px;
            height: 360px;
            position: absolute;
            top: 50%;
            left: 50%;
            .xtransform(-50%, -50%);
            text-align: center;
            h3{
                font-size: 20px;
                font-weight: 600;
            }
            .box-input{
                margin: 25px 0;
                .xdisplayflex();
                align-items: center;
                justify-content: center;
                i{
                    font-size: 50px;
                }
                input{
                    background: transparent;
                    width: 244px;
                    height: 18px;
                    padding: 15px;
                    font-size: 18px;
                    color: #fff;
                    border: 2px solid #fff;
                    border-radius: 5px;
                    outline: none;
                    margin-left: 14px;
                }
            }
        }
    }
</style>