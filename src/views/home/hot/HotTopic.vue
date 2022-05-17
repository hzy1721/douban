<script>
export default {
  name: "HotTopic",
  data() {
    return {
      topics: [
        {
          title: "看展记",
          titleUrl: "https://www.douban.com/gallery/topic/553/",
          isNew: false,
          visitNum: 9106.9,
        },
        {
          title: "寻找街头的镜子",
          titleUrl: "https://www.douban.com/gallery/topic/3329175/",
          isNew: true,
          visitNum: 6.0,
        },
        {
          title: "我接触过的那些阿尔茨海默症患者",
          titleUrl: "https://www.douban.com/gallery/topic/71675/",
          isNew: false,
          visitNum: 11.3,
        },
        {
          title: "你最不想在语文阅读理解中遇到谁的文章？",
          titleUrl: "https://www.douban.com/gallery/topic/17880/",
          isNew: false,
          visitNum: 38.9,
        },
        {
          title: "你遭遇过的校园霸凌",
          titleUrl: "https://www.douban.com/gallery/topic/85136/",
          isNew: false,
          visitNum: 24.5,
        },
        {
          title: "我的死亡焦虑",
          titleUrl: "https://www.douban.com/gallery/topic/81519/",
          isNew: false,
          visitNum: 20.3,
        },
      ],
    };
  },
};
</script>

<template>
  <h2>
    热门话题 · · · · · ·
    <span class="more"
      >( <a href="https://www.douban.com/gallery/">去话题广场</a> )</span
    >
  </h2>

  <div class="topic-item" v-for="topic in topics">
    <div>
      <a :href="topic.titleUrl" style="font-size: 14px">{{ topic.title }}</a>
    </div>
    <div class="subtitle">
      <span v-if="topic.isNew">新话题 · </span>
      <span>{{ topic.visitNum }}万次浏览</span>
    </div>
  </div>
</template>

<style>
.topic-item {
  margin-bottom: 15px;
}

.subtitle {
  color: #aaa;
}
</style>
