<script>
export default {
  data() {
    return {
      tags: "爱情 剧情 喜剧 悬疑 经典 动画 科幻 犯罪 动作 青春 搞笑 文艺 惊悚 励志 纪录片 黑色幽默 战争 家庭 美国 日本 香港 中国大陆 韩国 中国 英国 法国 台湾 印度".split(
        " "
      ),
    };
  },
};
</script>

<template>
  <div class="movie-category">
    <h2>
      影片分类 · · · · · ·
      <span class="more"
        >( <a href="https://movie.douban.com/tag/?view=type">更多</a> )</span
      >
    </h2>

    <div class="movie-tag" v-for="tag in tags">
      <a :href="'https://movie.douban.com/tag/' + tag">{{ tag }}</a>
    </div>
  </div>
</template>

<style>
.movie-tag {
  display: inline-block;
  width: 52px;
  margin-bottom: 4px;
}
</style>
