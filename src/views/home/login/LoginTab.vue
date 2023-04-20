<script>
import MessageLogin from "./MessageLogin.vue";
import PasswordLogin from "./PasswordLogin.vue";
import ThirdPartyLogin from "./ThirdPartyLogin.vue";

export default {
  data() {
    return {
      qrcodeLogin: false,
      tabIndex: 0,
    };
  },
  components: {
    MessageLogin,
    PasswordLogin,
    ThirdPartyLogin,
  },
};
</script>

<template>
  <div class="login-tab">
    <div class="switch-btn" @click="qrcodeLogin = !qrcodeLogin">
      <img loading="lazy" src="@/assets/home/login/switch_qrcode.png" v-show="!qrcodeLogin" />
      <img loading="lazy" src="@/assets/home/login/qrcode_login.png" v-show="qrcodeLogin" />
    </div>

    <template v-if="!qrcodeLogin">
      <div class="tab-bar">
        <div
          :class="['message-tab', { 'login-tab-active': tabIndex == 0 }]"
          @click="tabIndex = 0"
        >
          短信登录／注册
        </div>
        <div
          :class="['password-tab', { 'login-tab-active': tabIndex == 1 }]"
          @click="tabIndex = 1"
        >
          密码登录
        </div>
      </div>

      <MessageLogin v-show="tabIndex == 0" />

      <PasswordLogin v-show="tabIndex == 1" />

      <ThirdPartyLogin />
    </template>

    <template v-else>
      <div class="qrcode-login-title">二维码登录</div>
      <div class="qrcode-container">
        <img loading="lazy" src="@/assets/home/login/qrlogin_qrcode.png" />

        <div class="qrlogin-hint">
          请打开豆瓣 App 扫一扫 或
          <span
            class="switch-message-login"
            @click="(qrcodeLogin = false), (tabIndex = 0)"
            >短信登录验证</span
          >
        </div>
      </div>
    </template>
  </div>
</template>

<style>
.login-tab {
  width: 280px;
  position: absolute;
  top: 0;
  right: 0;
  padding: 10px;
}

.switch-btn {
  width: 30px;
  height: 30px;
  cursor: pointer;
  position: absolute;
  top: 10px;
  right: 10px;
}

.switch-btn img {
  width: 30px;
  height: 30px;
}

.login-tab .tab-bar {
  margin-top: 20px;
}

.message-tab,
.password-tab {
  display: inline-block;
  width: 50%;
  text-align: center;
  border-bottom: 1px solid #ececec;
  cursor: pointer;
  color: #9b9b9b;
  line-height: 2;
  font-family: Helvetica;
}

.login-tab-active {
  color: #333;
  font-weight: 600;
  border-bottom-color: #494949;
}

.qrcode-login-title {
  color: #333;
  font-weight: 600;
  text-align: left;
  border-bottom: 1px solid #ececec;
  margin-top: 20px;
  line-height: 2;
  font-family: Helvetica;
}

.qrcode-container {
  margin-top: 20px;
  text-align: center;
}

.qrcode-container img {
  width: 170px;
}

.qrlogin-hint {
  display: inline-block;
  color: #494949;
  margin-top: 3px;
  border-radius: 12px;
  padding: 3px 10px;
  background-color: rgba(0, 0, 0, 0.08);
  font-size: 13px;
}

.switch-message-login {
  color: #41ac52;
  cursor: pointer;
}
</style>
