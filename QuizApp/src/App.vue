<script setup>
import q from "./data/quizes.json";
import {ref, watch} from "vue";
import Card from "./components/Card.vue"

const quizes = ref(q);
const search = ref("");

watch(search, () => {
  quizes.value = q.filter(quiz => quiz.name.toLowerCase().includes(search.value.toLowerCase()));
})
</script>

<template>
  <div class="container">
    <header>
      <h1>Quizes</h1>
      <input v-model.trim="search" type="text" placeholder="Search...">
    </header>
    <div class="options-container">
      <Card v-for="quiz in quizes" :key="quiz.id" :quiz="quiz" />
    </div>
  </div>
</template>

<style scoped>
.container {
  max-width: 1000px;
  margin: 0 auto;
}

header {
  margin: 30px 0 10px;
  display: flex;
  align-items: center;
}

header h1 {
  margin-right: 30px;
  font-weight: 700;
}

header input {
  padding: 10px;
  border: none;
  outline: none;
  background-color: rgba(125,125,125,.1);
  border-radius: 5px;
}

.options-container {
  display: flex;
  flex-wrap: wrap;
  margin-top: 40px;
}
</style>