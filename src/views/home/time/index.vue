<script>
import ColumnItem from "./ColumnItem.vue";
import time_column_1 from '@/assets/home/time/time_column_1.jpg';
import time_column_2 from '@/assets/home/time/time_column_2.jpg';
import time_column_3 from '@/assets/home/time/time_column_3.jpg';
import time_column_4 from '@/assets/home/time/time_column_4.jpg';
import time_column_5 from '@/assets/home/time/time_column_5.jpg';
import time_column_6 from '@/assets/home/time/time_column_6.jpg';
import time_column_7 from '@/assets/home/time/time_column_7.png';
import time_column_8 from '@/assets/home/time/time_column_8.jpg';
import time_column_9 from '@/assets/home/time/time_column_9.jpg';
import time_column_10 from '@/assets/home/time/time_column_10.jpg';

export default {
  name: "TimeSection",
  data() {
    return {
      columns: [
        {
          imgUrl: time_column_1,
          title: "文学的甜头——如何成为一个真正的好读者",
          titleUrl: "https://m.douban.com/time/column/241",
          columnType: "音频",
        },
        {
          imgUrl: time_column_2,
          title: "重返思想的变迁时代——中国哲学16讲",
          titleUrl: "https://m.douban.com/time/column/242",
          columnType: "音频",
        },
        {
          imgUrl: time_column_3,
          title: "走出单一思维的陷阱——人类学思维18讲",
          titleUrl: "https://m.douban.com/time/column/240",
          columnType: "音频",
        },
        {
          imgUrl: time_column_4,
          title: "穿越文学经典——复旦梁永安的爱情课",
          titleUrl: "https://m.douban.com/time/column/230",
          columnType: "音频",
        },
        {
          imgUrl: time_column_5,
          title: "复旦沈奕斐的社会学爱情思维课",
          titleUrl: "https://m.douban.com/time/column/199",
          columnType: "音频",
        },
        {
          imgUrl: time_column_6,
          title: "和思想家一起漫步——20世纪留给我们的10种远见",
          titleUrl: "https://m.douban.com/time/column/229",
          columnType: "音频",
        },
        {
          imgUrl: time_column_7,
          title: "从未终结的历史——冷战12讲",
          titleUrl: "https://m.douban.com/time/column/239",
          columnType: "音频",
        },
        {
          imgUrl: time_column_8,
          title: "中国群星闪耀时——先秦诸子40讲",
          titleUrl: "https://m.douban.com/time/column/237",
          columnType: "音频",
        },
        {
          imgUrl: time_column_9,
          title: "说理与共识——学会与意见相左的人好好说话",
          titleUrl: "https://m.douban.com/time/column/238",
          columnType: "音频",
        },
        {
          imgUrl: time_column_10,
          title: "换种视角看世界——赵林的哲学思维入门课",
          titleUrl: "https://m.douban.com/time/column/236",
          columnType: "视频",
        },
      ],
    };
  },
  components: {
    ColumnItem,
  },
};
</script>

<template>
  <div>
    <h2 style="display: inline-block">
      <a href="https://time.douban.com/" class="time-title">豆瓣时间</a>
    </h2>

    <div class="hot-column">
      <h2>
        热门专栏 · · · · · ·
        <span class="more"
          >( <a href="https://time.douban.com/">更多</a> )</span
        >
      </h2>

      <ColumnItem
        class="column-item"
        v-for="column in columns"
        :imgUrl="column.imgUrl"
        :title="column.title"
        :titleUrl="column.titleUrl"
        :columnType="column.columnType"
      />
    </div>
  </div>
</template>

<style>
.time-title {
  font-size: 24px;
  color: #494949;
}

.hot-column {
  width: 800px;
  display: inline-block;
  vertical-align: top;
  margin-left: 30px;
  margin-top: 8px;
}

.column-item {
  display: inline-block;
  margin-right: 60px;
  margin-bottom: 30px;
  vertical-align: top;
}
</style>
