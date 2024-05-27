<script setup>
const props = defineProps({
  fishImgUrl: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <img class="h-14" :src="fishImgUrl" />
</template>

<style scoped></style>
