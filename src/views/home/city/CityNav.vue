<script>
export default {
  data() {
    return {
      subNavs: [
        {
          title: "近期活动",
          link: "https://www.douban.com/location/taiyuan/events",
        },
        {
          title: "主办方",
          link: "https://www.douban.com/location/taiyuan/hosts",
        },
        { title: "舞台剧", link: "https://www.douban.com/location/drama/" },
      ],
    };
  },
};
</script>

<template>
  <div class="city-nav">
    <div class="top-nav">
      <a href="https://www.douban.com/location/">同城</a>
    </div>

    <div class="sub-nav" v-for="nav in subNavs">
      <a :href="nav.link">{{ nav.title }}</a>
    </div>
  </div>
</template>

<style>
.city-nav {
  width: 100px;
  display: inline-block;
}

.city-nav .top-nav a {
  font-size: 24px;
  color: #ec5303;
}

.city-nav .top-nav a:hover {
  color: white;
}

.city-nav .sub-nav {
  font-size: 14px;
  margin-top: 5px;
}
</style>
