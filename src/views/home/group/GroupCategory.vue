<script>
export default {
  data() {
    return {
      groupTags: {
        兴趣: "旅行 摄影 影视 音乐 文学 游戏 动漫 运动 戏曲 桌游 怪癖".split(
          " "
        ),
        生活: "健康 美食 宠物 美容 化妆 护肤 服饰 公益 家庭 育儿 汽车".split(
          " "
        ),
        购物: "淘宝 二手 团购 数码 品牌 文具".split(" "),
        社会: "求职 租房 励志 留学 出国 理财 传媒 创业 考试".split(" "),
        艺术: "设计 手工 展览 曲艺 舞蹈 雕塑 纹身".split(" "),
        学术: "人文 社科 自然 建筑 国学 语言 宗教 哲学 软件 硬件 互联网".split(
          " "
        ),
        情感: "恋爱 心情 心理学 星座 塔罗 LES GAY".split(" "),
        闲聊: "吐槽 笑话 直播".split(" "),
      },
    };
  },
};
</script>

<template>
  <div class="group-category">
    <h2>小组分类 · · · · · ·</h2>

    <div class="tag-section" v-for="(tagList, tagCategory) in groupTags">
      <div class="tag-category">
        <a :href="`https://www.douban.com/group/explore?tag=${tagCategory}`">
          {{ tagCategory }}»
        </a>
      </div>
      <div class="tag-list">
        <div class="tag-item" v-for="tagItem in tagList">
          <a :href="`https://www.douban.com/group/explore?tag=${tagItem}`">
            {{ tagItem }}
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.group-category {
  display: inline-block;
  vertical-align: top;
  width: 260px;
  margin-bottom: 10px;
}

.group-category .tag-section {
  margin-bottom: 10px;
}

.group-category .tag-category {
  margin-bottom: 2px;
}

.group-category .tag-category a {
  color: #333 !important;
  font-size: 14px;
}

.group-category .tag-category a:hover {
  color: white !important;
}

.group-category .tag-list {
  margin-left: -12px;
}

.group-category .tag-item {
  display: inline-block;
  margin-left: 13px;
}
</style>
