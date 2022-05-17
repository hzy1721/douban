<script>
export default {
  props: ["imgUrl", "title", "titleUrl", "subtitle"],
};
</script>

<template>
  <div class="photo-title">
    <div>
      <a :href="titleUrl"><img :src="imgUrl" /></a>
    </div>
    <a :href="titleUrl">{{ title }}</a
    >&nbsp;
    <span class="subtitle">{{ subtitle }}</span>
  </div>
</template>

<style>
.photo-title {
  display: inline-block;
}

.photo-title img {
  width: 170px;
}

.photo-title .subtitle {
  color: #999;
}
</style>
