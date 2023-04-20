<script>
export default {
  name: "BannerSection",
};
</script>

<template>
  <div class="banner">
    <a href="https://www.douban.com/">
      <img loading="lazy" src="@/assets/home/banner/douban_logo.png" />
    </a>
  </div>
</template>

<style>
.banner {
  background-color: #edf4ec;
  line-height: 1.1;
}

.banner img {
  height: 20px;
  margin: 7px 13px;
}
</style>
