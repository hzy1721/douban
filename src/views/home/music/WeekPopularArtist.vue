<script>
import SubContentTitle from "../components/SubContentTitle.vue";
import popular_artist_1 from '@/assets/home/music/popular_artist_1.jpeg';
import popular_artist_2 from '@/assets/home/music/popular_artist_2.jpeg';
import popular_artist_3 from '@/assets/home/music/popular_artist_3.jpeg';
import popular_artist_4 from '@/assets/home/music/popular_artist_4.jpeg';
import popular_artist_5 from '@/assets/home/music/popular_artist_5.jpeg';

export default {
  data() {
    return {
      popularArtists: [
        {
          imgUrl: popular_artist_1,
          name: "Yamato Ryou",
          genre: "电子 Electronica",
          followNum: 302,
        },
        {
          imgUrl: popular_artist_2,
          name: "The NONAME",
          genre: "摇滚 Rock",
          followNum: 904,
        },
        {
          imgUrl: popular_artist_3,
          name: "LAVA|OX|SEA",
          genre: "摇滚 Rock",
          followNum: 1946,
        },
        {
          imgUrl: popular_artist_4,
          name: "JESSE CHOW",
          genre: "电子 Electronica",
          followNum: 1067,
        },
        {
          imgUrl: popular_artist_5,
          name: "Fading Horizon",
          genre: "摇滚 Rock",
          followNum: 1219,
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
  <div class="week-popular-artist">
    <SubContentTitle
      title="本周流行音乐人"
      moreLink="https://music.douban.com/artists/"
    />

    <div class="artist-item" v-for="(artist, index) in popularArtists">
      <span style="vertical-align: top">{{ index + 1 }}. </span>
      <img :src="artist.imgUrl" style="width: 48px; margin-left: 10px" />
      <div class="text-info">
        <div>
          <a :href="`https://site.douban.com/${artist.name}/`">{{
            artist.name
          }}</a>
        </div>
        <div style="color: #999">流派: {{ artist.genre }}</div>
        <div style="color: #999">{{ artist.followNum }}人关注</div>
      </div>
    </div>
  </div>
</template>

<style>
.week-popular-artist {
  display: inline-block;
  vertical-align: top;
  width: 265px;
  margin-left: 20px;
}

.artist-item {
  margin-bottom: 16px;
}

.artist-item .text-info {
  display: inline-block;
  vertical-align: top;
  margin-left: 10px;
}
</style>
