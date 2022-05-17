<script>
import BannerSection from "./banner/index.vue";
import TopNav from "./nav/index.vue";
import LoginSection from "./login/index.vue";
import HotSection from "./hot/index.vue";
import TimeSection from "./time/index.vue";
import MovieSection from "./movie/index.vue";
import GroupSection from "./group/index.vue";
import BookSection from "./book/index.vue";
import MusicSection from "./music/index.vue";
import MarketSection from "./market/index.vue";
import CitySection from "./city/index.vue";
import FooterSection from "./footer/index.vue";

export default {
  name: "HomeView",
  components: {
    BannerSection,
    TopNav,
    LoginSection,
    HotSection,
    TimeSection,
    MovieSection,
    GroupSection,
    BookSection,
    MusicSection,
    MarketSection,
    CitySection,
    FooterSection,
  },
};
</script>

<template>
  <BannerSection />

  <div class="nav-container">
    <TopNav class="top-nav" />
  </div>

  <div class="login-container">
    <LoginSection class="login-section" />
  </div>

  <div class="hot-container">
    <HotSection class="hot-section" />
  </div>

  <div class="time-container">
    <TimeSection class="time-section" />
  </div>

  <div class="movie-container">
    <MovieSection class="movie-section" />
  </div>

  <div class="group-container">
    <GroupSection class="group-section" />
  </div>

  <BookSection />

  <MusicSection />

  <MarketSection />

  <CitySection />

  <FooterSection />
</template>

<style>
.nav-container {
  padding-top: 30px;
  padding-bottom: 25px;
}

.top-nav {
  margin: 0 auto;
}

.login-container {
  background-color: #edf4ed;
  height: 304px;
  background-image: url("@/assets/home/login/login_banner_bg.jpg");
  background-repeat: no-repeat;
  background-position: calc(50% - 305px) 0;
  background-size: contain;
}

.login-section {
  margin: 0 auto;
  width: 950px;
}

.hot-container {
  padding: 25px 0;
}

.hot-section {
  width: 950px;
  margin: 0 auto;
}

.time-container {
  background-color: #f7f7f7;
  padding: 25px 0;
}

.time-section {
  width: 950px;
  margin: 0 auto;
}

.movie-container {
  padding: 25px 0;
}

.movie-section {
  width: 950px;
  margin: 0 auto;
}

.group-container {
  padding: 25px 0;
  background-color: #f7f7f7;
}

.group-section {
  width: 950px;
  margin: 0 auto;
}
</style>
