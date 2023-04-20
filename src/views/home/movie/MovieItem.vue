<script>
import ScoreShow from "@/components/ScoreShow.vue";

export default {
  props: ["imgUrl", "title", "titleUrl", "score", "buyUrl"],
  components: {
    ScoreShow,
  },
};
</script>

<template>
  <div class="movie-item">
    <div>
      <a :href="titleUrl">
        <img loading="lazy" class="movie-img" :src="imgUrl" />
      </a>
    </div>

    <div class="movie-title">
      <a :href="titleUrl">
        {{ title }}
      </a>
    </div>

    <ScoreShow :score="score" />

    <div class="buy-ticket">
      <a :href="buyUrl" class="buy-ticket">选座购票</a>
    </div>
  </div>
</template>

<style>
.movie-item {
  width: 110px;
  display: inline-block;
  vertical-align: top;
}

.movie-img {
  width: 100px;
  height: 150px;
}

.movie-title {
  text-align: center;
  margin-top: 10px;
}

.movie-title a {
  color: #333;
  font-size: 13px;
  line-height: 1.45;
  word-wrap: break-word;
  letter-spacing: normal;
  word-spacing: normal;
}

.movie-title a:hover {
  color: white;
}

.movie-score {
  text-align: center;
  margin-top: 1px;
  margin-bottom: 7px;
}

.movie-score .score-text {
  color: #e09015;
  margin-left: 4px;
}

.buy-ticket {
  text-align: center;
}

.buy-ticket a {
  color: #fff;
  background-color: #1c8bd0;
  padding: 4px 10px;
  border-radius: 2px;
  word-spacing: normal;
}

.buy-ticket a:hover {
  background-color: #27a;
}
</style>
