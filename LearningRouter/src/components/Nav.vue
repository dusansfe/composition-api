<script setup>
import { RouterLink } from 'vue-router';
</script>
<template>
    <div class="nav spacing">
        <RouterLink class="link" active-class="active" to="/">Home</RouterLink>
        <RouterLink class="link" active-class="active" to="/about">About</RouterLink>
    </div>
</template>

<style scoped>

.nav {
    padding-top: 20px;
    padding-bottom: 20px;
    background-color:darkkhaki;
}
.link {
    margin-right: 15px;
    text-decoration: none;
}
.link:last-of-type {
    margin-right: 0;
}
.active {
    color: royalblue;
}
</style>