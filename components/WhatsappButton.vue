<template>
  <div class="fixed bottom-5 right-5 z-50">
    <a
      :href="whatsappUrl"
      target="_blank"
      rel="noopener noreferrer"
      class="flex items-center justify-center w-14 h-14 rounded-full bg-green-500 text-white hover:bg-green-600 transition-colors duration-200"
    >
      <Icon name="logos:whatsapp-icon" class="text-3xl"/>
    </a>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  whatsappUrl: String
});
</script>
