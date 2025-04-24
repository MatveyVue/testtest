<template>
<div style="margin-top: 120px;" v-for="(person, index) in pack1" :key="index">
  <h3 class="name">{{ person.name }}</h3>
  <p class="avtor">{{ person.avtor }}</p>
  <p class="info">{{ person.info }}</p>
  <button class="star"><b>{{ person.stars }}</b></button>
</div>

<div class="carousel">
  <div class="carousel-inner" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
    <img class="stickers" v-for="(photo, index) in photos" :key="index" :src="photo" alt="Photo" loading="lazy"/>
  </div>
<button @click="prev" class="carousel-control prev">❮</button>
<button @click="next" class="carousel-control next">❯</button>
</div>

<inbox />

<div v-for="(person, index) in pack1" :key="index">
<button class="star">{{ person.stars }}</button>
</div>

<div style="color: rgb(41, 41, 41);">
<h1>.</h1>
<h1>.</h1>
</div>

</template>

<script>
import { pack1 } from '/src/script/pakss.js';
import inbox from '/src/views/Packs/isxodniks/inbox.vue'
import { ref } from 'vue';

export default {
components: {
    inbox,
},
data() {
  return {
  currentIndex: 0,
  photos: [
      'https://github.com/MatveyVue/icopn/blob/main/%D0%A1ap.png?raw=true',
      'https://github.com/MatveyVue/icopn/blob/main/%D0%A1ap.png?raw=true',
      'https://github.com/MatveyVue/icopn/blob/main/%D0%A1ap.png?raw=true',
      'https://github.com/MatveyVue/icopn/blob/main/%D0%A1ap.png?raw=true',
    ],

  pack1: [
    {
      name: "Hate Merch",
      avtor: "Whsxg",
      info: "A Meme Stickers a Hate Whsxg project",
      stars: "Pay for 100 stars",
    }
  ],
};
},
  methods: {
    next() {
      this.currentIndex = (this.currentIndex + 1) % this.photos.length;
    },
    prev() {
      this.currentIndex = (this.currentIndex - 1 + this.photos.length) % this.photos.length;
    },
  },
};
</script>

<style scoped>
body {
  background-color: rgb(41, 41, 41);
  touch-action: 0;
  overflow-x: hidden;
  background-attachment: fixed;
  -ms-overflow-style: none;
  scrollbar-width: none;
  overflow-y: hidden;
}

.name {
  font-family: Roboto;
  color: white;
  font-size: 24px;
}

.avtor {
  font-family: Roboto;
  color: white;
  font-size: 16px;
  margin-left: 2px;
}

.info {
  font-family: Roboto;
  color: white;
  font-size: 18px;
  margin-left: 2px;
  margin-top: 10px;
}

.star {
  width: 95%;
  position: fixed;
  height: 50px;
  bottom: 25px;
  margin-left: 1%;
  background-color: rgb(31, 129, 215);
  border-radius: 15px;
  border: none;
  font-family: Roboto;
  color: White;
  font-size: 16px;
}

.stickers {
  width: 100%;
}

.carousel {
  position: relative;
  overflow: hidden;
  margin-top: -65px;
}

.carousel-inner {
  display: flex;
  transition: transform 0.5s ease;
}

.carousel-item {
  min-width: 100%;
}

img {
  width: 100%;
}

.carousel-control {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(255,255,255,0.7);
  border: none;
  cursor: pointer;
}

.prev {
  background-color: rgba(39, 39,39,0);
  color: White;
  left: 0px;
  height: 100px;
  width: 25px;
  font-size: 32px;
}

.next {
  background-color: rgba(39, 39,39,0);
  color: White;
  right: 1px;
  height: 100px;
  width: 25px;
  font-size: 32px;
}
</style>
