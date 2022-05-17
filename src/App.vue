<script setup>
import { RouterView } from "vue-router";
</script>

<template>
  <RouterView />
</template>

<style>
body {
  font: 12px Helvetica, Arial, sans-serif;
  line-height: 1.62;
}

h2 {
  font: 15px Arial, Helvetica, sans-serif;
  color: #072;
}

a {
  text-decoration: none;
  color: #37a;
}

a:hover {
  color: white;
  background-color: #37a;
}

a img {
  border-width: 0;
  vertical-align: middle;
}

a img:hover {
  background-color: transparent;
}

.more {
  font: 12px Arial, Helvetica, sans-serif;
  color: #666;
}

input {
  outline: 0;
}
</style>
