<script setup>
import Fish from '@/Fish.vue'
const props = defineProps({
  fishesInAquarium: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <div class="h-screen bg-[url('../public/bg.jpg')]">
    <button v-for="fishImgUrl in fishesInAquarium" class="p-2">
      <Fish :fishImgUrl />
    </button>
  </div>
</template>
