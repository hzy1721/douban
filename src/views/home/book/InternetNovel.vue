<script>
import SubContentTitle from "../components/SubContentTitle.vue";
import internet_novel_1 from '@/assets/home/book/internet_novel_1.jpeg';
import internet_novel_2 from '@/assets/home/book/internet_novel_2.jpeg';
import internet_novel_3 from '@/assets/home/book/internet_novel_3.jpeg';
import internet_novel_4 from '@/assets/home/book/internet_novel_4.jpeg';

export default {
  data() {
    return {
      books: [
        {
          bookId: "382598897",
          imgUrl: internet_novel_1,
          title: "我在地府兼职判...",
          price: "免费",
          readId: "61437225",
        },
        {
          bookId: "386248147",
          imgUrl: internet_novel_2,
          title: "槿年",
          price: "免费",
          readId: "61791923",
        },
        {
          bookId: "381622335",
          imgUrl: internet_novel_3,
          title: "在春天",
          price: "免费",
          readId: "61341248",
        },
        {
          bookId: "389588664",
          imgUrl: internet_novel_4,
          title: "温度差",
          price: "免费",
          readId: "62006475",
        },
      ],
    };
  },
  methods: {
    bookLink(bookId) {
      return `https://read.douban.com/ebook/${bookId}/`;
    },
  },
  components: {
    SubContentTitle,
  },
};
</script>

<template>
  <div class="internet-novel">
    <SubContentTitle
      title="原创数字作品"
      moreText="更多"
      moreLink="https://read.douban.com/"
    />

    <div class="book-item" v-for="book in books">
      <div style="text-align: center">
        <a :href="bookLink(book.bookId)">
          <img loading="lazy" :src="book.imgUrl" style="width: 100px; height: 150px" />
        </a>
      </div>

      <div class="book-title">
        <a :href="bookLink(book.bookId)">
          {{ book.title }}
        </a>
      </div>

      <div class="book-price">{{ book.price }}</div>

      <div class="free-read">
        <a :href="`https://read.douban.com/reader/column/${book.readId}/`"
          >免费试读</a
        >
      </div>
    </div>
  </div>
</template>

<style>
.internet-novel {
  margin-bottom: 20px;
}

.book-item .book-price {
  text-align: center;
  color: #666;
  margin-bottom: 3px;
}
</style>
