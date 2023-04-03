<template>
  <div class="flex flex-col grow min-h-screen text-white bg-[url('./assets/background.png')]">
      <NavBar class="sticky top-0 z-50"/>  

      <div class="flex justify-center mx-auto mt-20 mb-auto w-3/4" v-if="['#/', '#', ''].includes(currentPath)">
        <Card />
      </div>
      <!--
      <div class="flex justify-center mx-auto mt-20 mb-auto w-4/5">
        <div class="flex flex-col mt-auto border-4 border-black border-opacity-90 rounded-lg shadow-xl mb-auto">
          <ImageCarousel />
        </div>
      </div>
      -->
      <Footer class="sticky mt-auto bottom-0 z-50" />
  </div>
</template>

<script setup>

import { ref, computed, h } from "vue";

import NavBar from './components/NavBar.vue';
import ImageCarousel from './components/ImageCarousel.vue';
import SimpleCard from './components/SimpleCard.vue';
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';

const currentPath = ref(window.location.hash || '#');

console.log('Initial currentPath:', currentPath.value);

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash;
  console.log('Updated currentPath:', currentPath.value);
});

</script>

<style scoped>
</style>
