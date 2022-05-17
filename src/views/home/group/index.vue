<script>
import GroupNav from "./GroupNav.vue";
import GroupHot from "./GroupHot.vue";
import GroupCategory from "./GroupCategory.vue";

export default {
  name: "GroupSection",
  components: {
    GroupNav,
    GroupHot,
    GroupCategory,
  },
};
</script>

<template>
  <div class="group-section">
    <GroupNav />

    <GroupHot class="group-hot" />

    <GroupCategory class="group-category" />
  </div>
</template>

<style>
.group-section a:link,
.group-section a:visited {
  color: #017a85;
}

.group-section a:hover {
  color: white;
}

.group-hot {
  margin-top: 8px;
  margin-left: 30px;
}

.group-category {
  margin-top: 8px;
}
</style>
