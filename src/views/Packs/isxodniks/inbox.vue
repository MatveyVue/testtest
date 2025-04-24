<template>
<h2 class="incom">Incoming stickers</h2>
<div v-for="(person, index) in pack1" :key="index" stick="contstick" style="display: flex; margin-left: -10px; overflow-x: scroll; overflow-y: hidden;">
    <div class="stickback">
        <img class="stick1" :src="person.stick1" alt="Cap" v-if="person.stick1">
    </div>
    <div class="stickback">
        <img class="stick1" :src="person.stick2" alt="Flag" v-if="person.stick2">
    </div>
    <div class="stickback">
        <img class="stick1" :src="person.stick1" alt="Cap" v-if="person.stick1">
    </div>
    <div class="stickback">
        <img class="stick1" :src="person.stick1" alt="Cap" v-if="person.stick1">
    </div>
</div>
</template>

<script setup>
import { pack1 } from './inbox.js';
</script>

<style scoped>
.incom {
    font-family: Roboto;
    color: White;
    font-size: 24px;
    margin-top: -25px;
}
</style>