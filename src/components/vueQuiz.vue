<template>
  <div class="progress">
    <div :style="{'width': percentage + '%'}"  class="progress__inner"></div>
  </div>
  <h1>{{ question.title }}</h1>
  <ul>
    <li
        v-for="(variant, i) in question.variants"
        :key="i"
        @click="onClickVariant(i, question.correct)">{{variant}}</li>
  </ul>
</template>

<script>
export default {
  name: "vueQuiz",
  props: {
    question: {
      type: Object,
      require: false
},
    percentage:{
      type: Number,
      require: false
    }
  },
  emits: {
    "nextStep": value => typeof value === "number"
  },
  methods: {
    onClickVariant(i, correct) {
      console.log(i, correct);
      this.$emit('nextStep', i, correct);
    }
  }
}
</script>

<style scoped>

</style>