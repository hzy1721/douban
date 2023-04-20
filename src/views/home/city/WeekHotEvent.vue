<script>
import SubContentTitle from "../components/SubContentTitle.vue";
import city_event_1 from '@/assets/home/city/city_event_1.jpeg';
import city_event_2 from '@/assets/home/city/city_event_2.jpeg';
import city_event_3 from '@/assets/home/city/city_event_3.jpeg';
import city_event_4 from '@/assets/home/city/city_event_4.jpeg';

export default {
  data() {
    return {
      events: [
        {
          id: "34808562",
          imgUrl: city_event_1,
          title: "布鹅岛乐队《午夜卑鄙电台》2022新专公路巡演 太原站",
          time: "5月20日 周五 20:30 - 22:00",
          location: "TheBoo 南中环街山西国际金...",
          followNum: 0,
        },
        {
          id: "34871121",
          imgUrl: city_event_2,
          title: "“甜蜜520”告白爱情电影主题视听音乐会《关于你的一...",
          time: "5月20日 周五 19:30 - 21:00",
          location: "青年宫演艺中心 府西街109号",
          followNum: 1,
        },
        {
          id: "34808466",
          imgUrl: city_event_3,
          title: "王晰“图景”个人巡回音乐会",
          time: "5月20日 周五 19:30 - 21:00",
          location: "山西大剧院 义井街道商务区...",
          followNum: 1,
        },
        {
          id: "34940819",
          imgUrl: city_event_4,
          title: "2022年山西优秀剧目展演《山西印象》民族管弦乐音乐会",
          time: "5月21日 周六 - 5月22日 周日",
          location: "山西大剧院 义井街道商务区...",
          followNum: 0,
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
  <div class="week-hot-event">
    <SubContentTitle
      title="太原 · 本周热门活动"
      moreLink="https://www.douban.com/location/"
    />

    <div class="event-item" v-for="event in events">
      <div class="cover-img">
        <a :href="`https://www.douban.com/event/${event.id}/`">
          <img loading="lazy" :src="event.imgUrl" style="width: 70px; height: 90px" />
        </a>
      </div>

      <div class="text-info">
        <div style="font-size: 13px; line-height: 1.45">
          <a :href="`https://www.douban.com/event/${event.id}/`">{{
            event.title
          }}</a>
        </div>

        <div style="margin-top: 4px; color: #666">
          <div>{{ event.time }}</div>
          <div>{{ event.location }}</div>
          <div>{{ event.followNum }}人关注</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.week-hot-event {
  width: 535px;
  margin-left: 30px;
  display: inline-block;
  vertical-align: top;
}

.week-hot-event .event-item {
  width: 247px;
  margin-right: 20px;
  margin-bottom: 20px;
  margin-top: 5px;
  display: inline-block;
  vertical-align: top;
}

.week-hot-event .event-item .cover-img {
  display: inline-block;
  vertical-align: top;
}

.week-hot-event .event-item .text-info {
  display: inline-block;
  vertical-align: top;
  margin-left: 10px;
  width: 167px;
}
</style>
