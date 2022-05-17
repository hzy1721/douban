<script>
import CityNav from "./CityNav.vue";
import WeekHotEvent from "./WeekHotEvent.vue";
import CityEventTag from "./CityEventTag.vue";

export default {
  name: "CitySection",
  components: {
    CityNav,
    WeekHotEvent,
    CityEventTag,
  },
};
</script>

<template>
  <div class="city-section">
    <div class="city-content">
      <CityNav />

      <WeekHotEvent />

      <CityEventTag />
    </div>
  </div>
</template>

<style>
.city-section {
  background-color: #f7f7f7;
  padding-top: 25px;
  padding-bottom: 35px;
}

.city-content {
  width: 950px;
  margin: 0 auto;
}

.city-content a {
  color: #643;
}

.city-content a:hover {
  color: white;
}
</style>
