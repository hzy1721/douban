<script>
import score_0 from '@/assets/global/score/score_0.png';
import score_1 from '@/assets/global/score/score_1.png';
import score_2 from '@/assets/global/score/score_2.png';
import score_3 from '@/assets/global/score/score_3.png';
import score_4 from '@/assets/global/score/score_4.png';
import score_5 from '@/assets/global/score/score_5.png';
import score_6 from '@/assets/global/score/score_6.png';
import score_7 from '@/assets/global/score/score_7.png';
import score_8 from '@/assets/global/score/score_8.png';
import score_9 from '@/assets/global/score/score_9.png';
import score_10 from '@/assets/global/score/score_10.png';

export default {
  props: ["score"],
  data() {
    return {
      scoreImgs: [
        score_0, score_1, score_2, score_3, score_4, score_5, 
        score_6, score_7, score_8, score_9, score_10,
      ]
    }
  }
};
</script>

<template>
  <div class="score-show">
    <template v-if="score >= 2">
      <img :src="scoreImgs[Math.round(score)]" />
      <span class="score-text">{{ score }}</span>
    </template>
    <template v-else> 暂无评分 </template>
  </div>
</template>

<style>
.score-show {
  text-align: center;
  margin-top: 3px;
  margin-bottom: 7px;
}

.score-text {
  color: #e09015;
  margin-left: 4px;
}
</style>
