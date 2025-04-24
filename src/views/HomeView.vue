<template> 
<h1 style="margin-top: 150px;" class="colls">Stickers collections</h1> 
<RouterLink to="Pack"> 
    <p class="see">See All</p> 
</RouterLink> 
<div id="banners"> 
<Banners  /> 
</div> 
   
<h1 class="free">Best Free Stickers</h1> 
<div id="freepack"> 
  <Free /> 
</div> 
   
<div id="pactostars"> 
  <Pack /> 
</div> 
   
<div style="color: rgb(41, 41, 41);"> 
<h1>.</h1> 
<h1>.</h1> 
<h1>.</h1> 
</div> 
   
<div id="bar"> 
  <Bar /> 
</div> 
</template> 
   
<script> 
import Pack from '../views/main/packsmain/pack.vue' 
import Free from '../views/main/freemain/free.vue' 
import Bar from './main/bar/bars.vue' 
import Banners from '../views/main/bannersmain/banners.vue' 
   
export default { 
  components: { 
    Pack, 
    Free, 
    Bar, 
    Banners, 
  } 
}; 
</script>