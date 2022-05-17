<script>
import SubContentTitle from "../components/SubContentTitle.vue";

export default {
  data() {
    return {
      topics: [
        {
          id: "225403601",
          title:
            "【申请已结束】一日三餐，一起吃饭：邀请各位爱晒猫的铲屎官免费试用新品「豆瓣猫咪餐具」",
          replyerNum: 685,
          date: "03-07",
        },
        {
          id: "203421229",
          title: "请开麦｜我们很想听听你的心声，期待豆瓣豆品出什么样的产品？",
          replyerNum: 197,
          date: "04-02",
        },
        {
          id: "204293834",
          title: "会员中心上线了「豆瓣遇见你便利贴」，100积分即可兑换",
          replyerNum: 13,
          date: "02-08",
        },
      ],
    };
  },
  components: {
    SubContentTitle,
  },
};
</script>

<template>
  <div class="official-group">
    <SubContentTitle
      title="官方小组"
      moreLink="https://www.douban.com/group/588598"
    />

    <div class="topic-item" v-for="topic in topics">
      <div class="topic-title">
        <a :href="`https://www.douban.com/group/topic/${topic.id}`">
          {{ topic.title }}
        </a>
      </div>

      <div class="bottom-info">
        <div class="replyer-num">{{ topic.replyerNum }} 人参与</div>
        <div class="topic-date">{{ topic.date }}</div>
      </div>
    </div>
  </div>
</template>

<style>
.official-group {
  margin-top: 30px;
}

.official-group .topic-item {
  margin-top: 5px;
  margin-bottom: 15px;
}

.official-group .topic-item .topic-title {
  font-size: 14px;
}

.official-group .topic-item .bottom-info {
  color: #6a6a6a;
  margin-top: 3px;
}

.official-group .topic-item .bottom-info div {
  display: inline-block;
  width: 50%;
}

.official-group .topic-item .bottom-info .topic-date {
  text-align: right;
}
</style>
