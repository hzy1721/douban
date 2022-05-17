<script>
export default {
  name: "HotNote",
  data() {
    return {
      headNote: {
        title: "叶芝和他的拜占庭诗篇",
        titleUrl: "https://www.douban.com/note/809888692/",
        author: "purplepine",
        preview:
          "去年四月，赋闲在家的我偶然地和一位朋友译起了叶芝的诗。此前我对这位二十世纪的大诗人和现代主义文学奠基人所知甚少，这样直接上手翻译，一开始自然如行雾中，但不带先入...",
      },
      notes: [
        {
          title: "男友为我过生日没花一分钱，该不该分手？",
          titleUrl: "https://www.douban.com/note/808856021/",
        },
        {
          title: "媒介蒙太奇 之 观看奥运",
          titleUrl: "https://www.douban.com/note/809257152/",
        },
        {
          title: "论家庭关系里好好说话的重要性",
          titleUrl: "https://www.douban.com/note/808006288/",
        },
        {
          title:
            "根据真实案件改编的悬疑小说：死去的人，真的会为了复仇而活过来吗？",
          titleUrl: "https://www.douban.com/note/808306604/",
        },
        {
          title: "两个月108公里，业余游泳爱好者路在何方",
          titleUrl: "https://www.douban.com/note/809408645/",
        },
        {
          title: "一名平凡读者的买书总结",
          titleUrl: "https://www.douban.com/note/809141061/",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="hot-note">
    <div>
      <div>
        <a :href="headNote.titleUrl">{{ headNote.title }}</a>
      </div>
      <div class="author">{{ headNote.author }}的日记</div>
      <div>{{ headNote.preview }}</div>
    </div>

    <div class="other-note" v-for="note in notes">
      <a :href="note.titleUrl">{{ note.title }}</a>
    </div>
  </div>
</template>

<style>
.hot-note {
  width: 275px;
  color: #666;
}

.hot-note .author {
  color: #999;
}

.hot-note .other-note {
  margin-top: 12px;
}
</style>
