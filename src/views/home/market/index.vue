<script>
import MarketNav from "./MarketNav.vue";
import HotSale from "./HotSale.vue";
import HotEvent from "./HotEvent.vue";
import OfficialGroup from "./OfficialGroup.vue";

export default {
  name: "MarketSection",
  components: {
    MarketNav,
    HotSale,
    HotEvent,
    OfficialGroup,
  },
};
</script>

<template>
  <div class="market-section">
    <div class="market-content">
      <MarketNav />

      <HotSale />

      <div class="right-part">
        <HotEvent />

        <OfficialGroup />
      </div>
    </div>
  </div>
</template>

<style>
.market-section {
  padding-top: 25px;
  padding-bottom: 35px;
}

.market-content {
  width: 950px;
  margin: 0 auto;
}

.market-content .right-part {
  display: inline-block;
  vertical-align: top;
  width: 265px;
  margin-left: 20px;
}
</style>
