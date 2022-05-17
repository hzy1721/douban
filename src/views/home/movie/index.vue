<script>
import MovieNav from "./MovieNav.vue";
import MovieShowing from "./MovieShowing.vue";
import MovieCategory from "./MovieCategory.vue";
import MovieRecentHot from "./MovieRecentHot.vue";

export default {
  name: "MovieSection",
  components: {
    MovieNav,
    MovieShowing,
    MovieCategory,
    MovieRecentHot,
  },
};
</script>

<template>
  <div>
    <MovieNav class="movie-nav" />

    <MovieShowing class="movie-showing" />

    <div class="right-side">
      <MovieCategory />

      <MovieRecentHot class="movie-recent-hot" />
    </div>
  </div>
</template>

<style>
.movie-nav {
  display: inline-block;
}

.movie-showing {
  display: inline-block;
  vertical-align: top;
  margin-top: 8px;
  margin-left: 30px;
}

.right-side {
  display: inline-block;
  vertical-align: top;
  margin-top: 8px;
  margin-left: 20px;
  width: 260px;
}

.movie-recent-hot {
  margin-top: 30px;
  margin-bottom: 30px;
}
</style>
