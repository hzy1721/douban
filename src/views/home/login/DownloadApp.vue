<script>
export default {
  data() {
    return {
      expandQrcode: false,
    };
  },
};
</script>

<template>
  <div class="download-app">
    <div class="title">
      豆瓣<span style="margin-left: 10px; font-weight: 100">7.0</span>
    </div>

    <div class="down-btn">
      <a href="https://www.douban.com/doubanapp/app?channel=nimingye"
        >下载豆瓣 App</a
      >
    </div>

    <div class="qrcode-part">
      <img
        src="@/assets/home/login/icon_qrcode_green.png"
        class="qrcode"
        v-show="!expandQrcode"
        @mouseover="expandQrcode = true"
      />
      <div
        class="expand-qrcode"
        v-show="expandQrcode"
        @mouseleave="expandQrcode = false"
      >
        <img src="@/assets/home/login/doubanapp_qrcode.png" />
        <p>iOS / Android 扫码直接下载</p>
      </div>
    </div>
  </div>
</template>

<style>
.download-app {
  display: inline-block;
}

.download-app .title {
  font-size: 25px;
  color: #111;
  margin-top: 3px;
  margin-bottom: 20px;
}

.down-btn {
  display: inline-block;
  background-color: #00b51d;
  padding: 9px 21px;
  border-radius: 2px;
  line-height: 1;
}

.down-btn a {
  font-size: 12px;
  color: white;
  background-color: #00b51d;
}

.download-app .qrcode-part {
  display: inline-block;
  margin-left: 5px;
}

.download-app .qrcode {
  width: 28px;
  vertical-align: middle;
  border: #00b51d 1px solid;
  border-radius: 2px;
}

.expand-qrcode {
  position: relative;
  display: inline-block;
  text-align: center;
  background-color: white;
  border-radius: 2px;
  padding: 18px;
  vertical-align: top;
  z-index: 2;
}

.expand-qrcode img {
  width: 150px;
}

.expand-qrcode p {
  color: #666;
  font-size: 13px;
  margin-top: 5px;
  margin-bottom: 0;
}
</style>
