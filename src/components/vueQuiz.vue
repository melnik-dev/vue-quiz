<template>
  <div class="progress">
    <div :style="{'width': '30%'}"  class="progress__inner"></div>
  </div>
  <h1>{{ question }}</h1>
  <ul>
    <li>Это функция для хранения данных компонента</li>
    <li>Это глобальный стейт</li>
    <li>Это когда на ты никому не нужен</li>
  </ul>
</template>

<script>
export default {
  name: "vueQuiz",
  props: ["question"]
}
</script>

<style scoped>

</style>