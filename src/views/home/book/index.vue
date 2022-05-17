<script>
import BookNav from "./BookNav.vue";
import NewBookExpress from "./NewBookExpress.vue";
import InternetNovel from "./InternetNovel.vue";
import BookHotTag from "./BookHotTag.vue";

export default {
  name: "BookSection",
  components: {
    BookNav,
    NewBookExpress,
    InternetNovel,
    BookHotTag,
  },
};
</script>

<template>
  <div class="book-section">
    <div class="book-content">
      <BookNav />

      <div class="middle-part">
        <NewBookExpress />

        <InternetNovel />
      </div>

      <BookHotTag />
    </div>
  </div>
</template>

<style>
.book-section {
  padding: 25px 0;
}

.book-content {
  width: 950px;
  margin: 0 auto;
}

.book-content a {
  color: #4a2f14;
}

.book-content a:hover {
  color: white;
}

.book-content .middle-part {
  display: inline-block;
  vertical-align: top;
  margin-left: 30px;
  width: 535px;
}
</style>
