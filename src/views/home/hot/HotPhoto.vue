<script>
import PhotoTitle from "./PhotoTitle.vue";
import hot_photo_1 from '@/assets/home/hot/hot_photo_1.webp';
import hot_photo_2 from '@/assets/home/hot/hot_photo_2.webp';
import hot_photo_3 from '@/assets/home/hot/hot_photo_3.webp';
import hot_photo_4 from '@/assets/home/hot/hot_photo_4.webp';

export default {
  name: "HotPhoto",
  data() {
    return {
      photos: [
        {
          imgUrl: hot_photo_1,
          title: "不能进入历史的历史",
          titleUrl: "https://www.douban.com/photos/album/1687237799/",
          photoNum: 19,
        },
        {
          imgUrl: hot_photo_2,
          title: "好好吃早饭",
          titleUrl: "https://www.douban.com/photos/album/1881849723/",
          photoNum: 330,
        },
        {
          imgUrl: hot_photo_3,
          title: "路过的路",
          titleUrl: "https://www.douban.com/photos/album/132170831/",
          photoNum: 161,
        },
        {
          imgUrl: hot_photo_4,
          title: "2020画画",
          titleUrl: "https://www.douban.com/photos/album/1873256890/",
          photoNum: 27,
        },
      ],
    };
  },
  components: {
    PhotoTitle,
  },
};
</script>

<template>
  <div class="photo-album">
    <PhotoTitle
      v-for="photo in photos"
      style="margin: 10px 0 0 10px"
      :imgUrl="photo.imgUrl"
      :title="photo.title"
      :titleUrl="photo.titleUrl"
      :subtitle="photo.photoNum + '张照片'"
    />
  </div>
</template>

<style>
.photo-album {
  width: 360px;
  margin: -10px 0 0 -10px;
}
</style>
