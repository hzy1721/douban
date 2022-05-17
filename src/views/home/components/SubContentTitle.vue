<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    moreText: {
      type: String,
      default: "更多",
    },
    moreLink: String,
  },
};
</script>

<template>
  <div class="sub-content-title">
    <span class="title">{{ title }} · · · · · ·</span>
    <span class="more" v-if="moreLink">
      ( <a :href="moreLink">{{ moreText }}</a> )
    </span>
  </div>
</template>

<style>
.sub-content-title {
  font: 15px Arial, Helvetica, sans-serif;
  color: #072;
  line-height: 40px;
}

.sub-content-title .more {
  font: 12px Arial, Helvetica, sans-serif;
  color: #666;
}
</style>
