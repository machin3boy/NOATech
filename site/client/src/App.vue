<script setup>
import NavBar from './components/NavBar.vue'
import Footer from './components/Footer.vue'
import MaintenanceCard from './components/MaintenanceCard.vue'

import { onMounted, ref } from 'vue'
import { initFlowbite } from 'flowbite'

// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
});

const currentPath = ref(window.location.hash || '#');

console.log('Initial currentPath:', currentPath.value);

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash;
  console.log('Updated currentPath:', currentPath.value);
});

</script>

<template>
  
  <div class="flex flex-col min-h-screen bg-gray-200" style="background-image: url('/src/assets/background.png')">

    <NavBar />

    <div class="mt-auto mb-auto justify-center w-3/4 mx-auto" v-if="['#/home', '#/', '#', ''].includes(currentPath)">
      <MaintenanceCard class="mt-20 mb-20"/>
    </div>

    <Footer class="mt-auto bottom-0 sticky"/>
    
  </div>
</template>

