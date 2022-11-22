<template>
    <div class="flex justify-center">
        <div class="block rounded-lg border-2 border-opacity-60 border-black shadow-lg bg-gray-600 max-w-sm text-center">
            <div class="py-3 px-6 border-b-2 border-gray-300 text-gray-100 text-xl">
                {{ header }}
            </div>
            <div class="p-6">
            <p class="text-gray-100 text-lg mb-4">
                {{ body }}
            </p>
            </div>
            <div class="py-3 px-6 border-t-2 border-gray-300 text-gray-100 text-lg">
                {{ footer }} 
            </div>
        </div>
    </div>
</template>

<script setup>
  defineProps(['header', 'body', 'footer']);
</script>
