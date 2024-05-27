<script setup>
import FishForm from "./FishForm.vue";
import Aquarium from "./Aquarium.vue";
import { ref } from "vue";

const fishesInAquarium = ref([
  "golden-purple-fish.png",
  "goldfish.png",
  "guppie.png",
  "tropical-fish.png",
  "tuna.png",
]);
const handleFishAdded = (fishAdded) => {
  fishesInAquarium.push(fishAdded);
};
</script>

<template>
  <div class="flex">
    <div class="flex flex-col w-1/6">
      <FishForm @fishAdded="handleFishAdded" />
    </div>
    <div class="flex flex-col w-5/6">
      <Aquarium :fishesInAquarium />
    </div>
  </div>
</template>
