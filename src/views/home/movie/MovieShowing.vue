<script>
import MovieItem from "./MovieItem.vue";
import showing_movie_1 from '@/assets/home/movie/showing_movie_1.webp';
import showing_movie_2 from '@/assets/home/movie/showing_movie_2.webp';
import showing_movie_3 from '@/assets/home/movie/showing_movie_3.webp';
import showing_movie_4 from '@/assets/home/movie/showing_movie_4.webp';
import showing_movie_5 from '@/assets/home/movie/showing_movie_5.webp';
import showing_movie_6 from '@/assets/home/movie/showing_movie_6.webp';
import showing_movie_7 from '@/assets/home/movie/showing_movie_7.webp';
import showing_movie_8 from '@/assets/home/movie/showing_movie_8.webp';

export default {
  data() {
    return {
      showingMovies: [
        {
          imgUrl: showing_movie_1,
          title: "坏蛋联盟",
          titleUrl: "https://movie.douban.com/subject/30165311/",
          score: 7.4,
          buyUrl: "https://movie.douban.com/subject/30165311/cinema/",
        },
        {
          imgUrl: showing_movie_2,
          title: "我是真的讨厌异...",
          titleUrl: "https://movie.douban.com/subject/35057107/",
          score: 0.0,
          buyUrl: "https://movie.douban.com/subject/35057107/cinema/",
        },
        {
          imgUrl: showing_movie_3,
          title: "神奇动物：邓布...",
          titleUrl: "https://movie.douban.com/subject/26147418/",
          score: 6.1,
          buyUrl: "https://movie.douban.com/subject/26147418/cinema/",
        },
        {
          imgUrl: showing_movie_4,
          title: "邓小平小道",
          titleUrl: "https://movie.douban.com/subject/35061625/",
          score: 0.0,
          buyUrl: "https://movie.douban.com/subject/35061625/cinema/",
        },
        {
          imgUrl: showing_movie_5,
          title: "致我的陌生恋人...",
          titleUrl: "https://movie.douban.com/subject/30402056/",
          score: 6.9,
          buyUrl: "https://movie.douban.com/subject/30402056/cinema/",
        },
        {
          imgUrl: showing_movie_6,
          title: "雷曼兄弟三部曲...",
          titleUrl: "https://movie.douban.com/subject/33459931/",
          score: 9.6,
          buyUrl: "https://movie.douban.com/subject/33459931/cinema/",
        },
        {
          imgUrl: showing_movie_7,
          title: "战马",
          titleUrl: "https://movie.douban.com/subject/25768090/",
          score: 9.1,
          buyUrl: "https://movie.douban.com/subject/25768090/cinema/",
        },
        {
          imgUrl: showing_movie_8,
          title: "葛饰北斋：超越...",
          titleUrl: "https://movie.douban.com/subject/27081074/",
          score: 8.5,
          buyUrl: "https://movie.douban.com/subject/27081074/cinema/",
        },
      ],
    };
  },
  components: {
    MovieItem,
  },
};
</script>

<template>
  <div class="movie-showing">
    <h2>
      正在热映 · · · · · ·
      <span class="more"
        >( <a href="https://movie.douban.com/showtimes/">更多</a> )</span
      >
    </h2>

    <MovieItem
      v-for="movie in showingMovies"
      :imgUrl="movie.imgUrl"
      :title="movie.title"
      :titleUrl="movie.titleUrl"
      :score="movie.score"
      :buyUrl="movie.buyUrl"
      class="movie-item"
    />
  </div>
</template>

<style>
.movie-showing {
  width: 540px;
}

.movie-item {
  margin: 0 12px 20px 12px;
}
</style>
