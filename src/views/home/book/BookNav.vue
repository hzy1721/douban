<script>
export default {
  data() {
    return {
      bookNavs: [
        {
          title: "分类浏览",
          link: "https://book.douban.com/tag/",
          isNew: false,
        },
        { title: "阅读", link: "https://read.douban.com/", isNew: true },
        {
          title: "作者",
          link: "https://book.douban.com/writers/",
          isNew: false,
        },
        {
          title: "书评",
          link: "https://book.douban.com/review/best/",
          isNew: false,
        },
        { title: "购书单", link: "https://book.douban.com/cart", isNew: false },
      ],
    };
  },
};
</script>

<template>
  <div class="book-nav">
    <div class="top-nav">
      <a href="https://book.douban.com/">读书</a>
    </div>

    <div class="sub-nav" v-for="nav in bookNavs">
      <a :href="nav.link">{{ nav.title }}</a>
      <img v-if="nav.isNew" src="@/assets/global/icon_new.gif" class="icon-new" />
    </div>

    <div class="read-app">
      <a href="https://read.douban.com/app/">
        <img src="@/assets/home/book/icon_read_app.jpg" class="app-icon" />
      </a>
      <div style="width: 50px; text-align: center; margin-top: 5px">
        <a href="https://read.douban.com/app/">豆瓣阅读</a>
      </div>
    </div>
  </div>
</template>

<style>
.book-nav {
  width: 100px;
  display: inline-block;
}

.book-nav .top-nav {
  font-size: 24px;
  margin-bottom: 10px;
}

.book-nav .sub-nav {
  font-size: 14px;
  margin-top: 5px;
}

.book-nav .read-app {
  margin-top: 15px;
}

.book-nav .app-icon {
  border-radius: 10px;
  box-shadow: 1px 1px 2px #999;
}
</style>
