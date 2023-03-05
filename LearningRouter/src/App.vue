<script setup>
import {RouterView} from "vue-router";
import Nav from "./components/Nav.vue";
</script>

<template>
 <div class="max-w-main">
  <Nav />
  <RouterView />
 </div>
</template>
