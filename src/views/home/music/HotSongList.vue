<script>
import SubContentTitle from "../components/SubContentTitle.vue";
import song_list_1 from '@/assets/home/music/song_list_1.jpeg';
import song_list_2 from '@/assets/home/music/song_list_2.jpeg';
import song_list_3 from '@/assets/home/music/song_list_3.jpeg';
import song_list_4 from '@/assets/home/music/song_list_4.jpeg';

export default {
  data() {
    return {
      songLists: [
        { id: "59122516", imgUrl: song_list_1, title: "乡村音乐" },
        { id: "15027024", imgUrl: song_list_2, title: "镜花水月" },
        { id: "251178", imgUrl: song_list_3, title: "一个人的演唱会" },
        { id: "323471", imgUrl: song_list_4, title: "deserts" },
      ],
    };
  },
  components: {
    SubContentTitle,
  },
};
</script>

<template>
  <div class="hot-song-list">
    <SubContentTitle
      title="热门歌单"
      moreLink="https://music.douban.com/programmes/"
    />

    <div class="song-list-item" v-for="songList in songLists">
      <div class="song-list-cover">
        <a :href="`https://music.douban.com/programme/${songList.id}`">
          <img loading="lazy" :src="songList.imgUrl" style="width: 80px" />
          <img loading="lazy" src="@/assets/home/music/icon_player.png" class="icon-overlay" />
        </a>
      </div>

      <div class="song-list-title">
        {{ songList.title }}
      </div>
    </div>
  </div>
</template>

<style>
.song-list-item {
  display: inline-block;
  vertical-align: top;
  width: 25%;
  text-align: center;
  margin-top: 5px;
}

.song-list-cover {
  position: relative;
  height: 80px;
}

.song-list-cover .icon-overlay {
  position: absolute;
  top: calc(50% - 22px);
  left: calc(50% - 22px);
}

.song-list-item .song-list-title {
  font-size: 13px;
  line-height: 1.45;
  margin-top: 10px;
}
</style>
