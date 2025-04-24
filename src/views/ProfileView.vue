<template>
  <div class="carousel">
    <div class="carousel-inner" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
      <div class="carousel-item" v-for="(photo, index) in photos" :key="index">
        <img :src="photo" alt="Photo" />
      </div>
    </div>
    <button @click="prev" class="carousel-control prev">❮</button>
    <button @click="next" class="carousel-control next">❯</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentIndex: 0,
      photos: [
        'https://github.com/MatveyVue/icopn/blob/main/%D0%A1ap.png?raw=true',
        'https://github.com/MatveyVue/icopn/blob/main/%D0%A1ap.png?raw=true',
        'https://github.com/MatveyVue/icopn/blob/main/%D0%A1ap.png?raw=true',
        'https://github.com/MatveyVue/icopn/blob/main/%D0%A1ap.png?raw=true',
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
.carousel {
  position: relative;
  overflow: hidden;
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
  left: 10px;
}

.next {
  right: 10px;
}
</style>