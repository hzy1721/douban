<template>
  <div class="movie-nav">
    <h2>
      <a href="https://movie.douban.com/" style="font-size: 24px"> 电影 </a>
    </h2>

    <div class="movie-nav-link">
      <div>
        <a href="https://movie.douban.com/nowplaying/">影讯&购票</a>
      </div>
      <div>
        <a href="https://movie.douban.com/explore">选电影</a>
        <img loading="lazy" src="@/assets/global/icon_new.gif" class="icon-new" />
      </div>
      <div>
        <a href="https://movie.douban.com/tv/">电视剧</a>
      </div>
      <div>
        <a href="https://movie.douban.com/chart">排行榜</a>
      </div>
      <div>
        <a href="https://movie.douban.com/tag/">分类</a>
      </div>
      <div>
        <a href="https://movie.douban.com/review/best/">影评</a>
      </div>
      <div>
        <a href="https://movie.douban.com/trailers">预告片</a>
      </div>
      <div>
        <a href="https://movie.douban.com/askmatrix/hot_questions/all">问答</a>
      </div>
    </div>
  </div>
</template>

<style>
.movie-nav {
  width: 100px;
}

.movie-nav-link {
  font-size: 14px;
}

.movie-nav-link div {
  margin-top: 5px;
}

.icon-new {
  width: 17px;
  height: 7px;
  vertical-align: top;
  position: relative;
  top: 4px;
  left: 3px;
}
</style>
