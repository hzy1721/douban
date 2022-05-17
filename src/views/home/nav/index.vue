<script>
export default {
  name: "NavSection",
  data() {
    return {
      searchText: "",
    };
  },
  methods: {
    submitSearch() {
      window.open(
        `https://www.douban.com/search?q=${this.searchText}`,
        "_blank"
      );
    },
  },
};
</script>

<template>
  <div class="home-top-nav">
    <div class="nav-left">
      <img
        src="@/assets/home/nav/sitename.png"
        style="width: 73px; height: 23px"
        class="sitename"
      />

      <div class="search-box">
        <input
          type="text"
          placeholder="书籍、电影、音乐、小组、小站、成员"
          id="nav-search"
          v-model="searchText"
        />
      </div>

      <div id="search-submit" @click="submitSearch"></div>
    </div>

    <span class="nav-titles">
      <a target="_blank" href="https://book.douban.com/">
        <img src="@/assets/home/nav/nav_book.png" />
      </a>
      <a target="_blank" href="https://movie.douban.com/">
        <img src="@/assets/home/nav/nav_movie.png" />
      </a>
      <a target="_blank" href="https://music.douban.com/">
        <img src="@/assets/home/nav/nav_music.png" />
      </a>
      <a target="_blank" href="https://www.douban.com/location/">
        <img src="@/assets/home/nav/nav_city.png" />
      </a>
      <a target="_blank" href="https://www.douban.com/group/">
        <img src="@/assets/home/nav/nav_group.png" />
      </a>
      <a target="_blank" href="https://read.douban.com/">
        <img src="@/assets/home/nav/nav_read.png" />
      </a>
      <a target="_blank" href="https://douban.fm/">
        <img src="@/assets/home/nav/nav_fm.png" />
      </a>
      <a target="_blank" href="https://time.douban.com/">
        <img src="@/assets/home/nav/nav_time.png" style="margin-bottom: 2px" />
      </a>
      <a target="_blank" href="https://market.douban.com/">
        <img src="@/assets/home/nav/nav_market.png" />
      </a>
    </span>
  </div>
</template>

<style>
.home-top-nav {
  width: 1080px;
}

.home-top-nav .nav-titles a img:hover {
  background-color: white;
}

.home-top-nav .sitename {
  vertical-align: middle;
}

.search-box {
  display: inline-block;
  vertical-align: middle;
  margin-left: 27px;
  width: 270px;
  height: 30px;
  border: rgb(190, 190, 190) 1px solid;
}

#nav-search {
  border: none;
  width: 240px;
  height: 20px;
  padding: 5px;
  font-size: 13px;
  margin-right: 3px;
}

#nav-search::placeholder {
  color: rgb(190, 190, 190);
}

#nav-search:focus {
  outline: none;
}

#search-submit {
  display: inline-block;
  cursor: pointer;
  background-image: url("@/assets/home/nav/nav_btn_search.png");
  width: 30px;
  height: 30px;
  vertical-align: middle;
  margin-left: -30px;
  border: 0;
  background-color: transparent;
  background-size: 14px;
  background-repeat: no-repeat;
  background-position: center;
}

.nav-left {
  display: inline-block;
  width: 50%;
}

.nav-titles {
  display: inline-block;
  text-align: right;
  vertical-align: middle;
  width: 50%;
}

.nav-titles a {
  margin-right: 18px;
}
</style>
