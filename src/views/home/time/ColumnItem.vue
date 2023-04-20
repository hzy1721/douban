<script>
export default {
  props: ["imgUrl", "title", "titleUrl", "columnType"],
};
</script>

<template>
  <div class="column-item">
    <div>
      <a :href="titleUrl">
        <img loading="lazy" :src="imgUrl" />
      </a>
    </div>

    <div class="column-title">
      <a :href="titleUrl">{{ title }}</a>
    </div>

    <div class="column-type">{{ columnType }}专栏</div>
  </div>
</template>

<style>
.column-item {
  width: 100px;
}

.column-item img {
  width: 100px;
}

.column-title {
  font-size: 13px;
  line-height: 1.38em;
  text-align: center;
  margin-top: 10px;
}

.column-title a {
  color: #333;
}

.column-item a:hover {
  color: white;
}

.column-type {
  color: #999;
  text-align: center;
  margin-top: 10px;
}
</style>
