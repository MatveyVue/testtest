<template>
<h1 style="margin-top: 120px;" class="colls">Stickers collections</h1>
<div class="backban">
<Banners />
</div>
</template>

<style scoped>
.backban {
    background-color: rgb(54, 54, 54);
    border-radius: 25px;
    height: 250px;
}

</style>

<script>
import Banners from '../views/all/bannersall.vue'

export default {
  components: {
    Banners,
  }
};
</script>
