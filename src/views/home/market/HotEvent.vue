<script>
import SubContentTitle from "../components/SubContentTitle.vue";

export default {
  components: {
    SubContentTitle,
  },
};
</script>

<template>
  <div class="hot-event">
    <SubContentTitle title="热门活动" />

    <div class="event-img">
      <a href="https://www.douban.com/gallery/topic/761/">
        <img loading="lazy" src="@/assets/home/market/hot_event.jpeg" />
      </a>
    </div>

    <div class="event-name">
      <a href="https://www.douban.com/gallery/topic/761/">
        我的豆瓣收藏夹里有什么
      </a>
    </div>
  </div>
</template>

<style>
.hot-event .event-img {
  margin-top: 5px;
}

.hot-event .event-img:hover {
  opacity: 0.8;
}

.hot-event .event-img img {
  width: 265px;
}

.hot-event .event-name {
  font-size: 14px;
  margin-top: 5px;
}
</style>
