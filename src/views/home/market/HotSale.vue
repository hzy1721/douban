<script>
import SubContentTitle from "../components/SubContentTitle.vue";
import hot_product_1 from '@/assets/home/market/hot_product_1.jpeg';
import hot_product_2 from '@/assets/home/market/hot_product_2.jpeg';
import hot_product_3 from '@/assets/home/market/hot_product_3.jpeg';
import hot_product_4 from '@/assets/home/market/hot_product_4.jpeg';

export default {
  data() {
    return {
      hotProducts: [
        {
          id: "weeklycalendar2022",
          name: "豆瓣读书周历2022",
          imgUrl: hot_product_1,
          price: 79,
        },
        {
          id: "bookfragrance",
          name: "国家图书馆 x 豆瓣 读书香薰",
          imgUrl: hot_product_2,
          price: 128,
        },
        {
          id: "calendar2022",
          name: "豆瓣电影日历2022",
          imgUrl: hot_product_3,
          price: 89,
        },
        {
          id: "doumaomoviefigure-2",
          name: "豆猫电影手办 · 第二弹",
          imgUrl: hot_product_4,
          price: 59,
        },
      ],
    };
  },
  components: {
    SubContentTitle,
  },
};
</script>

<template>
  <div class="hot-sale">
    <SubContentTitle title="热卖商品" moreLink="https://market.douban.com/" />

    <div class="product-item" v-for="product in hotProducts">
      <div class="product-img">
        <a :href="`https://market.douban.com/campaign/${product.id}`">
          <img :src="product.imgUrl" />
        </a>
      </div>

      <div style="margin-top: 10px">
        <div class="product-name">
          <a :href="`https://market.douban.com/campaign/${product.id}`">
            {{ product.name }}
          </a>
        </div>

        <div class="product-price">￥{{ product.price }}</div>
      </div>
    </div>
  </div>
</template>

<style>
.hot-sale {
  display: inline-block;
  vertical-align: top;
  width: 535px;
  margin-left: 30px;
}

.product-item {
  display: inline-block;
  vertical-align: top;
  width: 240px;
  margin-right: 20px;
  margin-bottom: 30px;
  margin-top: 5px;
}

.product-item .product-img:hover {
  opacity: 0.8;
}

.product-item .product-img img {
  width: 240px;
  height: 220px;
}

.product-item .product-name {
  display: inline-block;
  vertical-align: top;
  width: 190px;
  font-size: 16px;
  line-height: 22px;
}

.product-item .product-price {
  display: inline-block;
  vertical-align: top;
  width: 40px;
  margin-left: 10px;
  text-align: right;
  font-size: 16px;
  line-height: 22px;
  color: #e55457;
}
</style>
