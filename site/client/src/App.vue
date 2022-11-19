<template>
    <div class="flex flex-col grow min-h-screen text-white bg-orange-200 mb-10">
        <NavBar />  
        <div class="flex flex-col mx-10 mt-10 border-2 rounded-lg">
          <ImageCarousel />
        </div>
        <div class="flex flex-col wrap mx-10 mt-10 border-2 rounded-lg bg-red-300">
          <div class="my-10">
            <SimpleCard header="header text" body="body text" footer="footer text"/>
          </div>
        </div>
    </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue';
import ImageCarousel from './components/ImageCarousel.vue';
import SimpleCard from './components/SimpleCard.vue';
</script>

<style scoped>
</style>
