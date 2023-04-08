<template>
  <div>
    <div
      v-for="(item, index) in items"
      :key="item.title"
      :class="{
        'rounded-t-lg': index === 0,
        'border-t': index !== 0,
        'border-b': index !== items.length - 1
      }"
      class="border-gray-700/90"
    >
      <Disclosure as="div">
        <DisclosureButton
          :class="{
            'border-b-2 border-gray-700/95': index !== items.length - 1,
            'flex items-center justify-between w-full px-4 py-2 text-left font-bold text-white bg-gradient-to-r from-purple-800/95 to-teal-800/95': true,
            'rounded-t-lg': index === 0
          }"
        >
          <h2 class="text-lg">{{ item.title }}</h2>
          <svg
            class="w-6 h-6"
            fill="currentColor"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
              clip-rule="evenodd"
            ></path>
          </svg>
        </DisclosureButton>
        <DisclosurePanel
          :class="{
            'rounded-b-lg': index === items.length - 1
          }"
          class="p-4 text-white bg-gradient-to-r from-purple-700/90 to-teal-700/90"
          v-slot="{ open }"
        >
          <div v-if="open">
            {{ item.content }}
          </div>
        </DisclosurePanel>
      </Disclosure>
    </div>
  </div>
</template>



<script>
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue';

export default {
  components: {
    Disclosure,
    DisclosureButton,
    DisclosurePanel,
  },
  data() {
    return {
      items: [
        {
          title: 'Accordion Item 1',
          content: 'This is the content for the first accordion item.',
        },
        {
          title: 'Accordion Item 2',
          content: 'This is the content for the second accordion item.',
        },
        {
          title: 'Accordion Item 3',
          content: 'This is the content for the third accordion item.',
        },
      ],
    };
  },
};
</script>
