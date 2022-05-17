<script>
import HotPhoto from "./HotPhoto.vue";
import HotNote from "./HotNote.vue";

export default {
  name: "HotContent",
  components: {
    HotPhoto,
    HotNote,
  },
};
</script>

<template>
  <div>
    <h2>
      热点内容 · · · · · ·
      <span class="more">( <a href="/explore">更多</a> )</span>
    </h2>

    <HotPhoto class="albums" />

    <HotNote class="notes" />
  </div>
</template>

<style>
.albums {
  display: inline-block;
}

.notes {
  display: inline-block;
  vertical-align: top;
  margin-left: 30px;
}
</style>
