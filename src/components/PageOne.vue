<template>
  <div class="wrapper">
    <div id="web_bg"></div>
    <div class="nav-layout">
      <div class="logo"></div>
      <div class="nav-main">
        <div class="nav-item">首页</div>
        <div class="nav-item">渲染农场</div>
        <div class="nav-item">流程管理</div>
        <div class="nav-item">云网盘</div>
        <div class="nav-item">云审片</div>
        <div class="nav-item">云桌面</div>
      </div>
      <div class="nav-right">
        <div class="icon-news"></div>
        <div class="icon-news-text">未登录</div>
        <div class="icon-xl"></div>
      </div>
    </div>
    <div class="main-layout">
      <div class="flex-item">
        <div class="title"></div>
        <div class="content">
          <div class="left-layout">
            <div class="text-a">Welcome !</div>
            <div
              class="text-b"
            >We are improving the progress of optimization step by step. Welcome everyone to correct me.</div>
            <div class="text-c">© China Movie Cloud</div>
          </div>
          <div class="right-layout">
            <div class="text-a">欢迎登陆</div>
            <div
              class="text-b"
            >Welcome everyone to use the Chinese movie cloud.We hope you feel the best experience！</div>
            <div class="form-layout">
              <el-form
                ref="form"
                :model="form"
                :rules="rules"
                label-width="80px"
                label-position="top"
              >
                <el-form-item label="用户账号" prop="name">
                  <el-input v-model="form.name" placeholder="请输入用户账号"></el-input>
                </el-form-item>
                <el-form-item label="账号密码" prop="password">
                  <el-input v-model="form.password" placeholder="请输入账号密码"></el-input>
                </el-form-item>
              </el-form>
              <div style="overflow: hidden; margin-top: 10px">
                <div style="float: left">
                  立即
                  <span style="color: #3E3EFFFF">注册</span>
                </div>
                <div style="float: right; color:rgba(0,0,0,0.5);">忘记密码</div>
              </div>
              <el-button class="diy-btn" round @click="login">立即登录</el-button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {},
      rules: {
        name: [{ required: true, message: "请输入用户名", trigger: "blur" }],
        password: [{ required: true, message: "请输入密码", trigger: "change" }]
      }
    };
  },
  methods: {
    login() {
      this.$refs.form.validate(valid => {
        if (valid) {
          alert("submit!");
        } else {
          return false;
        }
      });
    }
  }
};
</script>

<style>
.el-form--label-top .el-form-item__label {
  padding: 0 !important;
}
.el-form-item {
  /* margin-bottom: 5px !important; */
}
@media screen and (max-width: 1500px) {
  .wrapper {
    zoom: 0.75;
  }
}
.diy-btn {
  margin-top: 40px !important;
  /* background: inherit; */
  background-image: url("../assets/juxing@2x.png") !important;
  border: none !important;
  width: 345px !important;
  height: 77px !important;
  background-size: 345px auto !important;
  background-repeat: no-repeat !important;
  color: #fff !important;
}
.wrapper {
}
.nav-layout {
  display: flex;
  padding: 25px 50px;
}
.nav-right {
  display: flex;
}
.nav-right .icon-news {
   background-image: url("../assets/icon_news@2x.png");
  width: 16px;
  height: 20px;
  background-size: 16px auto;
  background-repeat: no-repeat; 
}
.nav-right .icon-news-text {
  color: #fff;
  margin: 0 20px;
}
.nav-right .icon-xl {
  margin-top: 8px;
   background-image: url("../assets/icon_xl@2x.png");
  width: 12px;
  height: 6px;
  background-size: 12px auto;
  background-repeat: no-repeat; 
}

.nav-main {
  display: flex;
  flex: 1;
  padding: 0 400px;
}
.nav-main .nav-item {
  color: #fff;
  font-size: 18px;
  font-family: PingFangSC-Semibold, PingFang SC;
  font-weight: 600;
  color: rgba(255, 255, 255, 1);
  line-height: 25px;
  flex: 1;
  opacity: 0.5;
}
.nav-layout .logo {
  background-image: url("../assets/logo1@2x.png");
  width: 164px;
  height: 45px;
  background-size: 164px auto;
  background-repeat: no-repeat;
}
#web_bg {
  background-image: url("../assets/VCG41184067742@2x.png");
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  min-width: 1000px;
  z-index: -10;
  zoom: 1;
  background-color: #fff;
  background-repeat: no-repeat;
  background-size: cover;
  -webkit-background-size: cover;
  -o-background-size: cover;
  background-position: center 0;
}
.main-layout {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
}
.main-layout .title {
  background-image: url("../assets/name@2x.png");
  width: 550px;
  height: 95px;
  background-size: 550px auto;
  background-repeat: no-repeat;
}
.main-layout .flex-item {
  width: 1345px;
  height: 926px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.main-layout .content {
  background-image: url("../assets/fezu3@2x.png");
  width: 1198px;
  height: 724px;
  background-size: 1198px auto;
  background-repeat: no-repeat;
  position: relative;
}
.main-layout .content .right-layout {
  position: absolute;
  width: 334px;
  left: 705px;
  top: 97px;
  padding: 30px;
  text-align: left;
}
.main-layout .content .left-layout {
  position: absolute;
  width: 394px;
  left: 105px;
  top: 397px;
  padding: 30px;
  text-align: left;
  opacity: 0.7;
}
.right-layout .text-a {
  font-size: 30px;
  font-family: PingFangSC-Semibold, PingFang SC;
  font-weight: 600;
  color: rgba(0, 0, 0, 0.8);
  line-height: 42px;
}
.right-layout .text-b {
  font-size: 14px;
  font-family: PingFangSC-Regular, PingFang SC;
  font-weight: 400;
  color: rgba(0, 0, 0, 0.5);
  line-height: 20px;
}
.right-layout .form-layout {
  margin-top: 30px;
}
.left-layout .text-a {
  font-size: 40px;
  font-family: Arial-Black, Arial;
  font-weight: 900;
  color: rgba(255, 255, 255, 1);
  line-height: 56px;
}
.left-layout .text-b {
  margin-top: 20px;
  font-size: 14px;
  font-family: ArialMT;
  color: rgba(255, 255, 255, 1);
  line-height: 16px;
}
.left-layout .text-c {
  margin-top: 25px;
  font-size: 14px;
  font-family: ArialMT;
  color: rgba(255, 255, 255, 1);
  line-height: 16px;
}
</style>