<template>
  <div class="flex flex-col grow min-h-screen text-white bg-[url('./assets/background.png')]">
      <NavBar class="sticky top-0 z-50"/>  
      <div class="flex justify-center mx-auto mt-20 w-3/4">
        <Card />
      </div>
      <div class="flex justify-center mx-auto mt-20 mb-auto w-4/5">
        <div class="flex flex-col mt-auto border-4 border-black border-opacity-90 rounded-lg shadow-xl mb-auto">
          <ImageCarousel />
        </div>
      </div>
      <Footer class="sticky mt-20 bottom-0 z-50" />
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue';
import ImageCarousel from './components/ImageCarousel.vue';
import SimpleCard from './components/SimpleCard.vue';
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';

</script>

<style scoped>
</style>
