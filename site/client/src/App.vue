<template>
    <div class="flex flex-col grow min-h-screen text-white bg-[url('./assets/background.png')]">
        <NavBar class="sticky top-0 z-50"/>  
        <div class="flex flex-col mx-10 mt-10 border-4 border-black border-opacity-90 rounded-lg shadow-xl">
          <ImageCarousel />
        </div>
        <div id="about us">
          <div class="flex flex-col mx-10 mt-10 border-4 border-black border-opacity-90 rounded-lg shadow-xl bg-gradient-to-r from-indigo-300 to-cyan-300"> 
            <div class="flex mt-10 mx-auto md:ml-24 md:mr-auto">
              <div class="my-10 mx-auto">
                <SimpleCard header="header text" body="body text" footer="footer text"/>
              </div>
            </div>
            <div class="flex flex-wrap justify-evenly">
              <div class="my-10 mx-auto">
                <SimpleCard header="header text" body="body text" footer="footer text"/>
              </div>
              <div class="my-10 mx-auto">
                <SimpleCard header="header text" body="body text" footer="footer text"/>
              </div>
              <div class="my-10 mx-auto">
                <SimpleCard header="header text" body="body text" footer="footer text"/>
              </div>
              <div class="my-10 mx-auto">
                <SimpleCard header="header text" body="body text" footer="footer text"/>
              </div>
            </div>           
          </div>
        </div>        
        <div id="services">
          <div class="flex flex-col mx-10 mt-10 border-4 border-black border-opacity-90 rounded-lg bg-gradient-to-r from-red-400 to-red-300">
            <div class="flex mt-10 mx-auto md:ml-24 md:mr-auto">
              <div class="my-10 mx-auto">
                <SimpleCard header="header text" body="body text" footer="footer text"/>
              </div>
            </div>
            <div class="flex flex-wrap justify-evenly">
                <div class="my-10 mx-auto">
                  <SimpleCard header="header text" body="body text" footer="footer text"/>
                </div>
                <div class="my-10 mx-auto">
                  <SimpleCard header="header text" body="body text" footer="footer text"/>
                </div>
                <div class="my-10 mx-auto">
                  <SimpleCard header="header text" body="body text" footer="footer text"/>
                </div>
                <div class="my-10 mx-auto">
                  <SimpleCard header="header text" body="body text" footer="footer text"/>
                </div>
                <div class="my-10 mx-auto">
                  <SimpleCard header="header text" body="body text" footer="footer text"/>
                </div>
                <div class="my-10 mx-auto">
                  <SimpleCard header="header text" body="body text" footer="footer text"/>
                </div>
                <div class="my-10 mx-auto">
                  <SimpleCard header="header text" body="body text" footer="footer text"/>
                </div>
                <div class="my-10 mx-auto">
                  <SimpleCard header="header text" body="body text" footer="footer text"/>
                </div>
              </div>           
          </div>
        </div>
        <div class="mt-20">
          <Footer />
        </div>
    </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue';
import ImageCarousel from './components/ImageCarousel.vue';
import SimpleCard from './components/SimpleCard.vue';
import Footer from './components/Footer.vue';
</script>

<style scoped>
</style>
