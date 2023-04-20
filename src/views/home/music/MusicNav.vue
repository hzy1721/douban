<script>
export default {
  data() {
    return {
      musicNavs: [
        { title: "音乐人", link: "https://music.douban.com/artists/" },
        { title: "潮潮豆瓣音乐周", link: "https://www.douban.com/wetware/" },
        {
          title: "金羊毛计划",
          link: "https://music.douban.com/artists/royalty/",
        },
        { title: "专题", link: "https://music.douban.com/topics/" },
        { title: "排行榜", link: "https://music.douban.com/chart" },
        { title: "分类浏览", link: "https://music.douban.com/tag/" },
        { title: "乐评", link: "https://music.douban.com/review/latest/" },
        { title: "豆瓣FM", link: "https://douban.fm/" },
        { title: "歌单", link: "https://douban.fm/explore/songlists/" },
        { title: "阿比鹿音乐奖", link: "https://artist.douban.com/abilu/" },
      ],
    };
  },
};
</script>

<template>
  <div class="music-nav">
    <div class="top-nav">
      <a href="https://music.douban.com/">音乐</a>
    </div>

    <div class="sub-nav" v-for="nav in musicNavs">
      <a :href="nav.link">{{ nav.title }}</a>
    </div>

    <div class="app-nav">
      <a href="https://douban.fm/app">
        <img loading="lazy" src="@/assets/home/music/icon_fm_app.jpg" class="app-icon" />
      </a>
      <div class="app-title">
        <a href="https://douban.fm/app">豆瓣FM</a>
      </div>
    </div>

    <div class="app-nav">
      <a href="https://artist.douban.com/app">
        <img loading="lazy" src="@/assets/home/music/icon_artist_app.jpg" class="app-icon" />
      </a>
      <div class="app-title">
        <a href="https://artist.douban.com/app">豆瓣音乐人</a>
      </div>
    </div>
  </div>
</template>

<style>
.music-nav {
  width: 100px;
  display: inline-block;
}

.music-nav .top-nav {
  font-size: 24px;
  margin-bottom: 10px;
}

.music-nav .top-nav a {
  color: #f38c00;
}

.music-nav .top-nav a:hover {
  color: white;
}

.music-nav .sub-nav {
  font-size: 14px;
  margin-top: 5px;
}

.app-nav {
  margin-top: 15px;
}

.app-nav .app-icon {
  border-radius: 10px;
  box-shadow: 1px 1px 2px #999;
}

.app-nav .app-title {
  margin-top: 8px;
}
</style>
