<template>
  <div class="thirdparty-login">
    <span>第三方登录:</span>

    <a
      class="wechat-login"
      href="https://www.douban.com/accounts/connect/wechat/?from=&redir=https%3A//www.douban.com/"
    ></a>

    <a
      class="weibo-login"
      href="https://www.douban.com/accounts/connect/sina_weibo/?from=&redir=https%3A//www.douban.com/&fallback="
    ></a>
  </div>
</template>

<style>
.thirdparty-login {
  border-top: 1px solid #ddd;
  text-align: left;
  height: 40px;
}

.thirdparty-login span {
  color: #9b9b9b;
  font-size: 11px;
  line-height: 40px;
}

.thirdparty-login a {
  display: inline-block;
  margin-left: 10px;
  width: 32px;
  height: 32px;
  vertical-align: middle;
}

.thirdparty-login a:hover {
  background-color: transparent;
}

.wechat-login {
  background-image: url("@/assets/home/login/wechat_login_32.png");
}

.weibo-login {
  background-image: url("@/assets/home/login/weibo_login_32.png");
}
</style>
