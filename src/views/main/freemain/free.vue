<template>
<div style="margin-top: -10px;" class="freecont">
    <div style="margin-top: 35px;" v-for="(person, index) in fpack1" :key="index" class="ankets">
        <img class="freeicon" :src="person.icon" alt="Banner" v-if="person.icon">
        <p class="freenick"><b>{{ person.nick }}</b></p>
        <p class="coll">{{ person.coll }}</p>
        <button class="open"><b style="margin-left: -5px;">OPEN</b></button>
    </div>
</div>

<div style="margin-top: -5px;" class="freecont">
    <div style="margin-top: 35px;" v-for="(person, index) in fpack2" :key="index" class="ankets">
        <img class="freeicon" :src="person.icon" alt="Banner" v-if="person.icon">
        <p class="freenick"><b>{{ person.nick }}</b></p>
        <p class="coll">{{ person.coll }}</p>
        <button class="open"><b style="margin-left: -5px;">OPEN</b></button>
    </div>
</div>
</template>

<script setup>
import { fpack1, fpack2 } from './free.js';
</script>
