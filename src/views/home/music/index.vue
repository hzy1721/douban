<script>
import MusicNav from "./MusicNav.vue";
import MusicNewAlbum from "./MusicNewAlbum.vue";
import HotSongList from "./HotSongList.vue";
import WeekPopularArtist from "./WeekPopularArtist.vue";

export default {
  name: "MusicSection",
  components: {
    MusicNav,
    MusicNewAlbum,
    HotSongList,
    WeekPopularArtist,
  },
};
</script>

<template>
  <div class="music-section">
    <div class="music-content">
      <MusicNav />

      <div class="middle-part">
        <MusicNewAlbum />

        <HotSongList />
      </div>

      <WeekPopularArtist />
    </div>
  </div>
</template>

<style>
.music-section {
  padding-top: 25px;
  padding-bottom: 35px;
  background-color: #f7f7f7;
}

.music-content {
  width: 950px;
  margin: 0 auto;
}

.music-content a {
  color: #555d53;
}

.music-content a:hover {
  color: white;
}

.music-content .middle-part {
  display: inline-block;
  vertical-align: top;
  width: 535px;
  margin-left: 30px;
}
</style>
