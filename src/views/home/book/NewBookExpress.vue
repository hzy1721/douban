<script>
import SubContentTitle from "../components/SubContentTitle.vue";
import new_book_1 from '@/assets/home/book/new_book_1.jpeg';
import new_book_2 from '@/assets/home/book/new_book_2.jpeg';
import new_book_3 from '@/assets/home/book/new_book_3.jpeg';
import new_book_4 from '@/assets/home/book/new_book_4.jpeg';

export default {
  data() {
    return {
      books: [
        {
          bookId: "35574974",
          imgUrl: new_book_1,
          title: "世界上最丑的女...",
          author: "[波兰] 奥尔...",
          readId: "336703240",
        },
        {
          bookId: "35578828",
          imgUrl: new_book_2,
          title: "我们的家",
          author: "[日] 青山七...",
          readId: "335589245",
        },
        {
          bookId: "35369410",
          imgUrl: new_book_3,
          title: "混凝土岛",
          author: "[英] J.G...",
          readId: "329731612",
        },
        {
          bookId: "35560883",
          imgUrl: new_book_4,
          title: "气味之城",
          author: "文珍",
          readId: "333819477",
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
  <div class="new-book-express">
    <SubContentTitle
      title="新书速递"
      moreText="更多"
      moreLink="https://book.douban.com/latest"
    />

    <div class="book-item" v-for="book in books">
      <div style="text-align: center">
        <a :href="`https://book.douban.com/subject/${book.bookId}/`">
          <img loading="lazy" :src="book.imgUrl" style="width: 100px; height: 150px" />
        </a>
      </div>

      <div class="book-title">
        <a :href="`https://book.douban.com/subject/${book.bookId}/`">
          {{ book.title }}
        </a>
      </div>

      <div class="book-author">{{ book.author }}</div>

      <div class="free-read">
        <a :href="`https://read.douban.com/reader/ebook/${book.readId}/`"
          >免费试读</a
        >
      </div>
    </div>
  </div>
</template>

<style>
.new-book-express {
  margin-bottom: 20px;
}

.book-item {
  width: 110px;
  display: inline-block;
  vertical-align: top;
  margin: 5px 10px;
}

.book-item .book-title {
  text-align: center;
  font-size: 13px;
  margin-top: 10px;
  margin-bottom: 5px;
}

.book-item .book-author {
  text-align: center;
}

.book-item .free-read {
  text-align: center;
}

.book-item .free-read a {
  color: white;
  display: inline-block;
  padding: 2px 10px;
  background-color: #999a95;
  border-radius: 2px;
}

.book-item .free-read a:hover {
  background-color: #878882;
}
</style>
