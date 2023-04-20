<script>
import home_hot_ad from '@/assets/home/hot/home_hot_ad.jpg';

export default {
  name: "HotAd",
  data() {
    return {
      adUrl: "https://m.douban.com/time/column/241/",
      imgUrl: home_hot_ad,
    };
  },
};
</script>

<template>
  <div class="hot-ad">
    <a :href="adUrl">
      <img loading="lazy" :src="imgUrl" />
    </a>
    <div class="ad-symbol">广告</div>
  </div>
</template>

<style>
.hot-ad {
  position: relative;
  width: 250px;
  height: 125px;
}

.hot-ad img {
  width: 250px;
  height: 125px;
}

.ad-symbol {
  position: absolute;
  bottom: 0;
  right: 0;
  color: white;
  background-color: rgba(0, 0, 0, 0.3);
  padding: 4px;
  line-height: 1;
}
</style>
