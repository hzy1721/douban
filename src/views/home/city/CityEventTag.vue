<script>
import SubContentTitle from "../components/SubContentTitle.vue";

export default {
  data() {
    return {
      tagGroups: [
        {
          categoryName: "音乐",
          categoryId: "music",
          subTags: [
            { name: "小型现场", id: "1001" },
            { name: "音乐会", id: "1002" },
            { name: "演唱会", id: "1003" },
            { name: "音乐节", id: "1004" },
          ],
        },
        {
          categoryName: "戏剧",
          categoryId: "drama",
          subTags: [
            { name: "话剧", id: "1101" },
            { name: "音乐剧", id: "1102" },
            { name: "舞剧", id: "1103" },
            { name: "歌剧", id: "1104" },
            { name: "戏曲", id: "1105" },
            { name: "其他", id: "1106" },
          ],
        },
        {
          categoryName: "聚会",
          categoryId: "party",
          subTags: [
            { name: "生活", id: "1401" },
            { name: "集市", id: "1402" },
            { name: "摄影", id: "1403" },
            { name: "外语", id: "1404" },
            { name: "桌游", id: "1405" },
            { name: "夜店", id: "1406" },
            { name: "交友", id: "1407" },
            { name: "美食", id: "1408" },
            { name: "派对", id: "1409" },
          ],
        },
        {
          categoryName: "电影",
          categoryId: "film",
          subTags: [
            { name: "主题放映", id: "1801" },
            { name: "影展", id: "1802" },
            { name: "影院活动", id: "1803" },
          ],
        },
        {
          categoryName: "其他",
          categoryId: "all",
          subTags: [
            { name: "讲座", id: "salon" },
            { name: "展览", id: "exhibition" },
            { name: "运动", id: "sports" },
            { name: "旅行", id: "travel" },
            { name: "公益", id: "commonweal" },
          ],
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
  <div class="city-event-tag">
    <SubContentTitle title="活动标签" />

    <div class="tag-group" v-for="tagGroup in tagGroups">
      <div class="tag-category">
        <a
          :href="`https://www.douban.com/location/taiyuan/events/week-${tagGroup.categoryId}`"
        >
          {{ tagGroup.categoryName }}»
        </a>
      </div>

      <div class="sub-tag">
        <div class="sub-tag-item" v-for="tag in tagGroup.subTags">
          <a
            :href="`https://www.douban.com/location/taiyuan/events/week-${tag.id}`"
          >
            {{ tag.name }}
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.city-event-tag {
  width: 265px;
  margin-left: 20px;
  display: inline-block;
  vertical-align: top;
}

.city-event-tag .tag-group {
  margin-bottom: 10px;
}

.city-event-tag .tag-group .tag-category a {
  color: #333;
  font-size: 14px;
}

.city-event-tag .tag-group .tag-category a:hover {
  color: white;
}

.city-event-tag .tag-group .sub-tag {
  margin-top: 3px;
}

.city-event-tag .tag-group .sub-tag .sub-tag-item {
  display: inline-block;
  margin-right: 10px;
}
</style>
