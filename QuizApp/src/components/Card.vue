<script setup>
import {defineProps} from "vue";

const {quiz} = defineProps([
    'quiz'
])
</script>
<template>
    <div class="card">
        <img :src="quiz.img" :alt="quiz.name">
        <div class="card-text">
          <h2>{{quiz.name}}</h2>
          <p>{{quiz.questions.length}}</p>
        </div>
    </div>
</template>

<style scoped>
.card {
    width: 310px;
    overflow: hidden;
    border-radius: 2%;
    box-shadow: 1px 1px 10px rgba(0,0,0,0.1);
    margin-bottom: 35px;
    margin-right: 20px;
    cursor: pointer;
}

.card img {
    width: 100%;
    height: 200px;
    margin: 0;
}

.card .card-text {
    padding: 0 10px 10px;
}

.card .card-text h2 {
    font-weight: 600;
}
</style>