<template>
    <div class="flex flex-col grow min-h-screen text-white bg-orange-200">
        <NavBar />  
        <div class="flex flex-col mx-10 my-10 border-2 rounded-lg">
          <ImageCarousel />
        </div>
    </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue';
import ImageCarousel from './components/ImageCarousel.vue';
</script>

<style scoped>
</style>
