<script setup>
import {ref} from 'vue';

const activeIndex = ref(0) 

const images = [
  {
    fullSize: 'https://images.unsplash.com/photo-1618700997914-1a62d43cda70?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80'
  },
  {
    fullSize: 'https://images.unsplash.com/photo-1599074914978-2946b69e5a4a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80'
  },
  {
    fullSize: 'https://images.unsplash.com/photo-1549300461-11c5b94e8855?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80'
  },
  {
    fullSize: 'https://images.unsplash.com/photo-1599074914978-2946b69e5a4a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80'
  },  
]

</script>

<template>
    <div id="carouselExampleDark" class="carousel carousel-dark slide" data-bs-ride="carousel">
      <div class="carousel-inner">

        <div class="carousel-item active">
          <img :src="images[activeIndex].fullSize" class="d-block w-100" alt="...">
          <div class="carousel-caption d-none d-md-block">
          </div>
        </div>
        
      </div>
      <button @click="0 == activeIndex ? activeIndex = (images.length) - 1 : activeIndex-- " class="carousel-control-prev" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span>Previous</span>
      </button>
      <button @click="(images.length) - 1 == activeIndex ? activeIndex = 0 : activeIndex++" class="carousel-control-next" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="next">
        <span>Next</span> 
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
      </button>
    </div>
</template>

<style scoped>

</style>
