<script setup>
import NavBar from './components/NavBar.vue'
import Footer from './components/Footer.vue'
import SolutionsAccordion from './components/SolutionsAccordion.vue'
import MaintenanceCard from './components/MaintenanceCard.vue'
import ContactBox from './components/ContactBox.vue'

import { onUpdated, ref } from 'vue'
import { initFlowbite } from 'flowbite'

// initialize components based on data attribute selectors
onUpdated(() => {
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
  <div class="flex flex-col min-h-screen bg-cover bg-[url('./assets/background_2x2_purple_dark.png')] object-cover" style="height: 100vh;">
    <NavBar />

    <!-- HOME CONTENT -->
    <div class="flex-1 flex justify-center items-center box-sizing border-box" v-if="['#/home', '#/', '#', ''].includes(currentPath)">
      <MaintenanceCard class="mt-20 mb-20 mx-5" />
    </div>

    <!-- ABOUT CONTENT-->
    <div class="my-10 mx-10 mt-20 overflow-y-auto" v-if="currentPath === '#/about'">
      <SolutionsAccordion />
    </div>

    <!-- CONTANT CONTENT-->
    <div class="mx-3 my-auto overflow-y-auto" v-if="currentPath === '#/contact'">
      <ContactBox />
    </div>
    
    <Footer class="mt-auto bottom-0 sticky mb-2" />
  </div>
</template>
