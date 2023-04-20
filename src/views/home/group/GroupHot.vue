<script>
import hot_group_1 from '@/assets/home/group/hot_group_1.webp';
import hot_group_2 from '@/assets/home/group/hot_group_2.webp';
import hot_group_3 from '@/assets/home/group/hot_group_3.webp';
import hot_group_4 from '@/assets/home/group/hot_group_4.webp';
import hot_group_5 from '@/assets/home/group/hot_group_5.webp';
import hot_group_6 from '@/assets/home/group/hot_group_6.webp';
import hot_group_7 from '@/assets/home/group/hot_group_7.webp';
import hot_group_8 from '@/assets/home/group/hot_group_8.webp';

export default {
  data() {
    return {
      hotGroups: [
        { id: "echofans", name: "我爱三毛", memberNum: 48561 },
        { id: "shafake", name: "沙发客", memberNum: 22737 },
        { id: "liucixin", name: "刘慈欣", memberNum: 32518 },
        { id: "20618", name: "西双版纳", memberNum: 12915 },
        { id: "402725", name: "记事本圆梦小组", memberNum: 117411 },
        { id: "170177", name: "这辈子一定要做几件疯狂的事", memberNum: 93335 },
        { id: "cuthair", name: "自己给自己剪头发", memberNum: 36457 },
        { id: "83759", name: "我们就是要做衣服给自己穿", memberNum: 3632 },
      ],
      groupImgs: [
        hot_group_1, hot_group_2, hot_group_3, hot_group_4, 
        hot_group_5, hot_group_6, hot_group_7, hot_group_8,
      ]
    };
  },
};
</script>

<template>
  <div class="group-hot">
    <h2>
      热门小组 · · · · · ·
      <span class="more"
        >( <a href="https://movie.douban.com/showtimes/">更多</a> )</span
      >
    </h2>

    <div class="group-item" v-for="(group, index) in hotGroups">
      <a :href="`https://www.douban.com/group/${group.id}/`" class="group-img">
        <img loading="lazy" :src="groupImgs[index]" />
      </a>

      <div class="right-text">
        <div class="group-name">
          <a :href="`https://www.douban.com/group/${group.id}/`">
            {{ group.name }}
          </a>
        </div>
        <div class="member-num">{{ group.memberNum }} 个成员</div>
      </div>
    </div>
  </div>
</template>

<style>
.group-hot {
  display: inline-block;
  vertical-align: top;
  width: 556px;
}

.group-item {
  display: inline-block;
  margin-top: 30px;
  margin-right: 30px;
  width: 248px;
}

.group-item .group-img {
  display: inline-block;
  width: 48px;
  height: 48px;
  margin-right: 15px;
  margin-bottom: 10px;
}

.group-item img {
  width: 48px;
  height: 48px;
}

.group-item .right-text {
  display: inline-block;
  vertical-align: top;
}

.group-item .group-name a {
  font-size: 13px;
  line-height: 1.45;
}

.group-item .member-num {
  color: #999;
  margin-top: 5px;
}
</style>
