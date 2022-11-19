<template>
    <div class="flex justify-center">
        <div class="block rounded-lg shadow-lg bg-white max-w-sm text-center">
            <div class="py-3 px-6 border-b border-gray-300 text-gray-600 text-xl">
                {{ header }}
            </div>
            <div class="p-6">
            <p class="text-gray-700 text-lg mb-4">
                {{ body }}
            </p>
            </div>
            <div class="py-3 px-6 border-t border-gray-300 text-gray-600 text-lg">
                {{ footer }} 
            </div>
        </div>
    </div>
</template>

<script setup>
  defineProps(['header', 'body', 'footer']);
</script>
