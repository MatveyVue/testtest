<template>
<div class="banners">
    <div v-for="(person, index) in banners1" :key="index" class="ankets">
        <img class="banner" :src="person.icon" alt="Banner" v-if="person.icon">
        <img class="icon" :src="person.icon" alt="Banner" v-if="person.icon">
        <p class="nick"><b>{{ person.nick }}</b></p>
    </div>
</div>
</template>
    
<style scoped>
.banner {
    width: 96vw;
    margin-left: -40px;
    min-width: 200px;
}

.icon {
    margin-top: 208px;
    width: 30px;
    height: 30px;
}

.nick  {
    margin-top: 8px;
}
</style>

<script setup>
import { banners1 } from './bannersall.js'
</script>