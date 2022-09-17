<template>
  <div class="result">
    <img src="https://cdn-icons-png.flaticon.com/512/2278/2278992.png"/>
    <h2>Вы отгадали {{ correct }} ответа из {{ questions.length }}</h2>
    <a href="/">
      <button>Попробовать снова</button>
    </a>
  </div>
</template>

<script>
export default {
  name: "vueResult",
  props: {
    correct: {
      type: Number,
      require: false
    },
    questions: {
      type: Array,
      require: false
    }
  },
}
</script>

<style scoped>

</style>