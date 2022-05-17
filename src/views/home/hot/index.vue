<script>
import HotContent from "./HotContent.vue";
import HotAd from "./HotAd.vue";
import HotTopic from "./HotTopic.vue";

export default {
  name: "HotSection",
  components: {
    HotContent,
    HotAd,
    HotTopic,
  },
};
</script>

<template>
  <div class="hot-section">
    <HotContent class="hot-content" />

    <div class="right-part">
      <HotAd />

      <HotTopic />
    </div>
  </div>
</template>

<style>
.hot-content {
  display: inline-block;
  vertical-align: top;
}

.hot-section .right-part {
  display: inline-block;
  vertical-align: top;
  margin-top: 0.83em;
  margin-left: 30px;
  width: 250px;
}
</style>
