<script>
import SubContentTitle from "../components/SubContentTitle.vue";
import ScoreShow from "@/components/ScoreShow.vue";
import new_album_1 from '@/assets/home/music/new_album_1.jpeg';
import new_album_2 from '@/assets/home/music/new_album_2.jpeg';
import new_album_3 from '@/assets/home/music/new_album_3.jpeg';
import new_album_4 from '@/assets/home/music/new_album_4.jpeg';
import new_album_5 from '@/assets/home/music/new_album_5.jpeg';
import new_album_6 from '@/assets/home/music/new_album_6.jpeg';
import new_album_7 from '@/assets/home/music/new_album_7.jpeg';
import new_album_8 from '@/assets/home/music/new_album_8.jpeg';

export default {
  data() {
    return {
      newAlbums: [
        {
          id: "35807125",
          imgUrl: new_album_1,
          title: "梦境",
          artist: "大象体操",
          score: 7.5,
        },
        {
          id: "35889930",
          imgUrl: new_album_2,
          title: "杜康",
          artist: "GAI周延",
          score: 6.2,
        },
        {
          id: "35891850",
          imgUrl: new_album_3,
          title: "也是蓝",
          artist: "也是福",
          score: 7.1,
        },
        {
          id: "35812771",
          imgUrl: new_album_4,
          title: "石敢当",
          artist: "木推瓜",
          score: 8.8,
        },
        {
          id: "35874188",
          imgUrl: new_album_5,
          title: "Mr. Morale & The Big Steppers",
          artist: "Kendrick Lamar",
          score: 8.7,
        },
        {
          id: "35875237",
          imgUrl: new_album_6,
          title: "A Light For Attracting Attention",
          artist: "The Smile",
          score: 9.0,
        },
        {
          id: "35868669",
          imgUrl: new_album_7,
          title: "minisode2：Thursday's Child",
          artist: "TXT TOMORROW X TOGETHER 투모로우바이투게더",
          score: 7.4,
        },
        {
          id: "35863961",
          imgUrl: new_album_8,
          title: "FEARLESS",
          artist: "LE SSERAFIM 르세라핌",
          score: 6.2,
        },
      ],
    };
  },
  methods: {
    albumLink(id) {
      return `https://music.douban.com/subject/${id}/`;
    },
  },
  components: {
    SubContentTitle,
    ScoreShow,
  },
};
</script>

<template>
  <div class="music-new-album">
    <SubContentTitle
      title="豆瓣新碟榜"
      moreText="更多"
      moreLink="https://music.douban.com/#new1"
    />

    <div class="album-item" v-for="(album, index) in newAlbums">
      <div class="album-cover">
        <a :href="albumLink(album.id)">
          <img loading="lazy" :src="album.imgUrl" />
        </a>
      </div>

      <div class="album-title">
        {{ index + 1 }}.
        <a :href="albumLink(album.id)">
          {{ album.title }}
        </a>
      </div>

      <div class="album-artist">
        {{ album.artist }}
      </div>

      <ScoreShow :score="album.score" />
    </div>
  </div>
</template>

<style>
.music-new-album .album-item {
  width: 25%;
  display: inline-block;
  vertical-align: top;
  text-align: center;
  margin-top: 5px;
}

.music-new-album .album-item .album-cover img {
  width: 80px;
  max-height: 120px;
}

.music-new-album .album-title {
  margin-top: 10px;
  margin-bottom: 3px;
}
</style>
