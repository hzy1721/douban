<script>
import DownloadApp from "./DownloadApp.vue";
import LoginTab from "./LoginTab.vue";

export default {
  name: "LoginSection",
  components: {
    DownloadApp,
    LoginTab,
  },
};
</script>

<template>
  <div class="login-section">
    <DownloadApp class="download-app" />

    <LoginTab />
  </div>
</template>

<style>
.login-section {
  height: 100%;
  position: relative;
}

.download-app {
  height: 120px;
  margin-left: 50%;
  margin-top: 90px;
}
</style>
