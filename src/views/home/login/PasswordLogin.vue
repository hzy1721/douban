<script>
export default {
  name: "PasswordLogin",
};
</script>

<template>
  <div class="password-login">
    <div class="retrieve-password">
      <a href="https://accounts.douban.com/passport/get_password">找回密码</a>
    </div>

    <div class="input-box">
      <input type="text" placeholder="手机号 / 邮箱" />
    </div>

    <div class="input-box">
      <input type="password" placeholder="密码" />
    </div>

    <div class="login-submit">登录豆瓣</div>

    <div class="oversea-phone-login">海外手机登录</div>
  </div>
</template>

<style>
.retrieve-password {
  margin: 10px 0;
  text-align: right;
}

.retrieve-password a {
  color: #41ac52;
}

.retrieve-password a:hover {
  background-color: transparent;
}

.password-login .input-box {
  position: relative;
  margin-bottom: 10px;
}

.password-login input {
  box-sizing: border-box;
  width: 280px;
  font-size: 13px;
  border: 1px solid #e4e6d5;
  border-radius: 3px;
  padding: 8px 10px;
}

.oversea-phone-login {
  text-align: right;
  margin: 10px 0;
  color: #41ac52;
  font-size: 13px;
  cursor: pointer;
}
</style>
