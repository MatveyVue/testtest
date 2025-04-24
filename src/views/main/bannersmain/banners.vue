<template>
<div class="banners">
    <div v-for="(person, index) in banners1" :key="index" class="ankets">
        <img class="banner" :src="person.icon" alt="Banner" v-if="person.icon">
        <img class="icon" :src="person.icon" alt="Banner" v-if="person.icon">
        <p class="nick"><b>{{ person.nick }}</b></p>
    </div>
    <div v-for="(person, index) in banners1" :key="index" class="ankets">
        <img class="banner" :src="person.icon" alt="Banner" v-if="person.icon">
        <img class="icon" :src="person.icon" alt="Banner" v-if="person.icon">
        <p class="nick"><b>{{ person.nick }}</b></p>
    </div>
</div>
</template>

<script setup>
import { banners1 } from './banners.js'
</script>