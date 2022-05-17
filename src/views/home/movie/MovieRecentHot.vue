<script>
export default {
  data() {
    return {
      recentHotMovies: [
        {
          title: "坏蛋联盟",
          url: "https://movie.douban.com/subject/30165311/",
        },
        {
          title: "神奇动物：邓布利多之谜",
          url: "https://movie.douban.com/subject/26147418/",
        },
        {
          title: "365天：今时之欲",
          url: "https://movie.douban.com/subject/35464873/",
        },
        {
          title: "四海",
          url: "https://movie.douban.com/subject/35337517/",
        },
        {
          title: "套装",
          url: "https://movie.douban.com/subject/35372415/",
        },
        {
          title: "神秘海域",
          url: "https://movie.douban.com/subject/3822687/",
        },
        {
          title: "亡命救护车",
          url: "https://movie.douban.com/subject/35250237/",
        },
        {
          title: "新蝙蝠侠",
          url: "https://movie.douban.com/subject/6424756/",
        },
        {
          title: "长津湖之水门桥",
          url: "https://movie.douban.com/subject/35613853/",
        },
        {
          title: "东北告别天团",
          url: "https://movie.douban.com/subject/35871767/",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="movie-recent-hot">
    <h2>
      近期热门 · · · · · ·
      <span class="more"
        >( <a href="https://movie.douban.com/chart">更多</a> )</span
      >
    </h2>

    <div class="recent-hot-item" v-for="(movie, index) in recentHotMovies">
      <span>{{ index + 1 }}. &nbsp;</span>
      <a :href="movie.url">{{ movie.title }}</a>
    </div>
  </div>
</template>

<style>
.recent-hot-item {
  border-bottom: 1px solid #eaeaea;
  padding-bottom: 5px;
  margin-bottom: 6px;
}
</style>
