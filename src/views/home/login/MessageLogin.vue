<script>
export default {
  name: "MessageLogin",
};
</script>

<template>
  <div class="message-login">
    <div class="login-agreement">
      请仔细阅读
      <a href="https://accounts.douban.com/passport/agreement">
        豆瓣使用协议、豆瓣个人信息保护政策
      </a>
    </div>

    <div class="input-box">
      <div class="area-code">+86</div>
      <input type="text" placeholder="手机号" class="phone-input" />
    </div>

    <div class="input-box">
      <input type="text" placeholder="验证码" class="verify-code-input" />
      <div class="request-verify-code">获取验证码</div>
    </div>

    <div class="login-submit">登录豆瓣</div>

    <div class="cannot-receive-code">
      <a href="https://help.douban.com/account?app=1#t1-q5">收不到验证码</a>
    </div>
  </div>
</template>

<style>
.login-agreement {
  color: #9b9b9b;
  margin: 10px 0;
}

.login-agreement a {
  color: #41ac52;
}

.login-agreement a:hover {
  background-color: transparent;
}

.message-login input {
  box-sizing: border-box;
  width: 280px;
  font-size: 13px;
  border: 1px solid #e4e6d5;
  border-radius: 3px;
  padding-top: 8px;
  padding-bottom: 8px;
}

.message-login .input-box {
  position: relative;
  margin-bottom: 10px;
}

.area-code {
  position: absolute;
  top: 5px;
  left: 0;
  width: 50px;
  font-size: 15px;
  font-weight: bold;
  text-align: center;
  cursor: pointer;
  border-right: 1px solid #dfdfdf;
}

.phone-input {
  padding-left: 60px;
  padding-right: 40px;
}

.verify-code-input {
  padding-left: 10px;
  padding-right: 10px;
}

.request-verify-code {
  position: absolute;
  top: 0;
  right: 10px;
  cursor: pointer;
  width: 65px;
  height: 35px;
  line-height: 35px;
  color: #41ac52;
  font-size: 13px;
}

.login-submit {
  width: 280px;
  height: 34px;
  background-color: #41ac52;
  border-radius: 3px;
  color: white;
  text-align: center;
  line-height: 34px;
  font-size: 15px;
  cursor: pointer;
}

.cannot-receive-code {
  text-align: right;
  margin: 10px 0;
}

.cannot-receive-code a {
  color: #41ac52;
  font-size: 13px;
}

.cannot-receive-code a:hover {
  background-color: transparent;
}
</style>
