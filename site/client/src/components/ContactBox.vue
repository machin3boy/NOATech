<template>
    <div class="bg-gradient-to-r from-purple-700/90 to-teal-700/90 p-8 rounded-2xl">
      <h2 class="text-2xl font-bold text-white mb-6 text-center">Contact Us</h2>
      <form @submit.prevent="submitForm">
        <div class="mb-4">
          <label for="message" class="block text-white">Message</label>
          <textarea
            id="message"
            v-model="message"
            class="w-full h-32 px-3 py-2 bg-white-900/95 rounded-md shadow-inner"
            required
          ></textarea>
        </div>
  
        <div class="grid grid-cols-2 gap-4">
          <div class="mb-4">
            <label for="email" class="block text-white">Email</label>
            <input
              id="email"
              v-model="email"
              type="email"
              class="w-full px-3 py-2 bg-white-900/95 rounded-md shadow-inner"
              required
            />
          </div>
          <div class="mb-4">
            <label for="business" class="block text-white">Business (optional)</label>
            <input
              id="business"
              v-model="business"
              type="text"
              class="w-full px-3 py-2 bg-white-900/95 rounded-md shadow-inner"
            />
          </div>
        </div>
  
        <div class="grid grid-cols-2 gap-4">
          <div class="mb-4">
            <label for="name" class="block text-white">Name (optional)</label>
            <input
              id="name"
              v-model="name"
              type="text"
              class="w-full px-3 py-2 bg-white-900/95 rounded-md shadow-inner"
            />
          </div>
          <div class="mb-4">
            <label for="phone" class="block text-white">Phone (optional)</label>
            <input
              id="phone"
              v-model="phone"
              type="tel"
              class="w-full px-3 py-2 bg-white-900/95 rounded-md shadow-inner"
            />
          </div>
        </div>
  
        <button
          type="submit"
          class="w-full py-2 text-white bg-purple-800/90 hover:bg-purple-900/90 rounded-md"
        >
          Send
        </button>
      </form>
    </div>
  
    <Dialog v-if="isOpen" :open="isOpen" @close="setIsOpen(false)" class="fixed inset-0 z-10">
      <DialogOverlay class="fixed inset-0" />
      <DialogPanel class="bg-gradient-to-r from-purple-700/90 to-teal-700/90 p-8 m-auto rounded-2xl mt-20 w-11/12 sm:w-1/2 md:w-1/3 lg:w-1/4">
        <DialogTitle class="text-2xl font-bold text-white mb-6 text-center">Message Sent</DialogTitle>
        <DialogDescription class="text-xl text-white mb-8 text-center">
          Your message has been sent successfully!
        </DialogDescription>
        <button
          @click="setIsOpen(false)"
          class="w-full py-2 text-white bg-purple-800/90 hover:bg-purple-900/90 rounded-md"
        >
          Close
        </button>
      </DialogPanel>
    </Dialog>

</template>
    
<script setup>
  import { ref } from 'vue';
  import { Dialog, DialogOverlay, DialogPanel, DialogTitle, DialogDescription } from '@headlessui/vue';

  const message = ref('');
  const name = ref('');
  const business = ref('');
  const email = ref('');
  const phone = ref('');
  const isOpen = ref(false);

  const emailRegex = /^[\w-]+(\.[\w-]+)*@([\w-]+\.)+[a-zA-Z]{2,7}$/;

  function setIsOpen(value) {
    isOpen.value = value;
  }

  function submitForm() {
    if (message.value && emailRegex.test(email.value)) {
      console.log({
        message: message.value,
        name: name.value,
        business: business.value,
        email: email.value,
        phone: phone.value,
      });

      // Clear form fields
      message.value = '';
      name.value = '';
      business.value = '';
      email.value = '';
      phone.value = '';

      // Open the dialog/modal
      setIsOpen(true);
    } else {
      alert('Please fill out the required fields.');
    }
  }
</script>
