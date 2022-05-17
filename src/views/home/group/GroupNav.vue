<script>
export default {
  data() {
    return {
      groupNavs: [
        { title: "精选", link: "https://www.douban.com/group/explore" },
        { title: "文化", link: "https://www.douban.com/group/explore/culture" },
        { title: "行摄", link: "https://www.douban.com/group/explore/travel" },
        { title: "娱乐", link: "https://www.douban.com/group/explore/ent" },
        { title: "时尚", link: "https://www.douban.com/group/explore/fashion" },
        { title: "生活", link: "https://www.douban.com/group/explore/life" },
        { title: "科技", link: "https://www.douban.com/group/explore/tech" },
      ],
    };
  },
};
</script>

<template>
  <div class="group-nav">
    <h2>
      <a href="https://www.douban.com/group/" style="font-size: 24px"> 小组 </a>
    </h2>

    <div class="group-nav-link">
      <div v-for="nav in groupNavs">
        <a :href="nav.link">{{ nav.title }}</a>
      </div>
    </div>
  </div>
</template>

<style>
.group-nav {
  display: inline-block;
  width: 100px;
}

.group-nav-link div {
  font-size: 14px;
  margin-top: 5px;
}
</style>
