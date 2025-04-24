<template>
<div>
<div style="margin-top: -10px;" v-for="(person, index) in pack1" :key="index" class="ankets">
<RouterLink style="text-decoration: none;" to="Pack1">
    <h1 class="namestick">{{ person.nick }}</h1>
    <p class="avtor">{{ person.avtor }}</p>
</RouterLink>
<div style="margin-top: -5px;" v-for="(person, index) in pack1" :key="index">
    <button class="starsbtn"><img class="star" src="/src/components/Stars.png"><p class="starcol">{{ person.stars }}</p></button>
</div>
<div class="contstick" style="display: flex">
    <div class="stickback">
        <img class="stick1" :src="person.stick1" alt="Cap" v-if="person.stick1">
    </div>
    <div class="stickback">
        <img class="stick1" :src="person.stick2" alt="Flag" v-if="person.stick2">
    </div>
    <div class="stickback">
        <img class="stick1" :src="person.stick1" alt="Cap" v-if="person.stick1">
    </div>
</div>
</div>
</div>

<div>
<div style="margin-top: -10px;" v-for="(person, index) in pack1" :key="index" class="ankets">
<RouterLink style="text-decoration: none;" to="Pack2">
    <h1 class="namestick">{{ person.nick }}</h1>
    <p class="avtor">{{ person.avtor }}</p>
</RouterLink>
<div style="margin-top: -5px;" v-for="(person, index) in pack1" :key="index">
    <button class="starsbtn"><img class="star" src="/src/components/Stars.png"><p class="starcol">{{ person.stars }}</p></button>
</div>
<div class="contstick" style="display: flex">
    <div class="stickback">
        <img class="stick1" :src="person.stick1" alt="Cap" v-if="person.stick1">
    </div>
    <div class="stickback">
        <img class="stick1" :src="person.stick2" alt="Flag" v-if="person.stick2">
    </div>
    <div class="stickback">
        <img class="stick1" :src="person.stick1" alt="Cap" v-if="person.stick1">
    </div>
</div>
</div>
</div>
</template>

<script setup>
import { pack1, pack2 } from './pack.js';
</script>
