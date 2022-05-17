<script>
import SubContentTitle from "../components/SubContentTitle.vue";

export default {
  data() {
    return {
      hotTags: {
        文学: "小说 随笔 日本文学 散文 诗歌 童话 名著 港台".split(" "),
        流行: "漫画 推理 绘本 科幻 青春 言情 奇幻 武侠".split(" "),
        文化: "历史 哲学 传记 设计 建筑 电影 回忆录 音乐".split(" "),
        生活: "旅行 励志 教育 职场 美食 灵修 健康 家居".split(" "),
        经管: "经济学 管理 商业 金融 营销 理财 股票 企业史".split(" "),
        科技: "科普 互联网 编程 交互设计 算法 通信 神经网络".split(" "),
      },
    };
  },
  components: {
    SubContentTitle,
  },
};
</script>

<template>
  <div class="book-hot-tag">
    <SubContentTitle
      title="热门标签"
      moreText="更多"
      moreLink="https://book.douban.com/tag/?view=type"
    />

    <div>
      <div v-for="(tagList, tagCategory, index) in hotTags" class="tag-group" :key="index">
        <span class="tag-category">[{{ tagCategory }}]</span>
        <div class="tag-item" v-for="(tag, index) in tagList" :key="index">
          <a :href="`https://book.douban.com/tag/${tag}`">
            {{ tag }}
          </a>
        </div>
        <div class="tag-item">
          <a :href="`https://book.douban.com/tag/?view=type#${tagCategory}`"
            >更多</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.book-hot-tag {
  display: inline-block;
  vertical-align: top;
  width: 265px;
  margin-left: 20px;
}

.book-hot-tag .tag-group {
  padding: 10px 0;
}

.book-hot-tag .tag-group:not(:first-child) {
  border-top: 1px solid #eaeaea;
}

.book-hot-tag .tag-category {
  color: #999;
  margin-right: 10px;
}

.book-hot-tag .tag-item {
  display: inline-block;
  margin-right: 10px;
}
</style>
