<template>
  <div class="wrapper">
    <div id="web_bg"></div>
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
              <el-form ref="form" :model="form" label-width="80px" label-position="top">
                <el-form-item label="用户账号">
                  <el-input v-model="form.name"></el-input>
                </el-form-item>
                <el-form-item label="账号密码">
                  <el-input v-model="form.name"></el-input>
                </el-form-item>
              </el-form>
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
      form: {}
    };
  }
};
</script>

<style>
.el-form--label-top .el-form-item__label {
  padding: 0 !important;
}
@media screen and (max-width: 1500px) {
  .wrapper {
    /* zoom: 0.75; */
  }
}
.wrapper {
  display: flex;
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
  width: 150px;
  height: 42px;
  font-size: 30px;
  font-family: PingFangSC-Semibold, PingFang SC;
  font-weight: 600;
  color: rgba(0, 0, 0, 0.8);
  line-height: 42px;
}
.right-layout .text-b {
  width: 313px;
  height: 40px;
  font-size: 14px;
  font-family: PingFangSC-Regular, PingFang SC;
  font-weight: 400;
  color: rgba(0, 0, 0, 0.5);
  line-height: 20px;
}
.right-layout .form-layout {
  margin-top: 20px;
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