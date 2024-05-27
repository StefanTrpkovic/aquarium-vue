<script setup>
import { ref } from "vue";
import Fish from "./Fish.vue";

const fishesImgUrl = ref([
  "golden-purple-fish.png",
  "goldfish.png",
  "guppie.png",
  "tropical-fish.png",
  "tuna.png",
]);

const fishName = ref("");
</script>
<template>
  <div class="flex-col p-5">
    <h1 class="text-white font-bold">Fish Type</h1>
    <div class="flex flex-wrap pt-4">
      <button v-for="fishImgUrl in fishesImgUrl" class="p-2">
        <Fish :fishImgUrl />
      </button>
    </div>
    <h1 class="text-white font-bold pt-6">Name</h1>
    <input type="text" class="rounded w-full h-9" v-model="fishName" />
    <button
      class="bg-red-800 w-full h-9 rounded mt-5"
      @click="$emit('fishAdded', { fishName, fishNumber: 1 })"
    >
      Add Fish
    </button>
  </div>
</template>
<style scoped></style>
