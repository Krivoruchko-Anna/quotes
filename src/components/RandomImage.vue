<script setup lang="ts">
import { computed } from "vue";
import { NUMBER_OF_IMAGES } from "@/constants";

const randomPicture = computed(() => {
  const randomImageNumber = Math.floor(Math.random() * NUMBER_OF_IMAGES) + 1
  return `images/random/image_${randomImageNumber}.jpg`
})
</script>

<template>
  <img class="quotes__image" :src="randomPicture" alt="image">
</template>

<style lang="scss">
.quotes__image {
  min-width: 330px;
  width: 330px;
  height: fit-content;
  margin-top: 56px;
  border-radius: 4px;
  filter: saturate(0.7);

  @media (max-width: 1180px) {
    float: right;
    margin-bottom: 30px;
    margin-left: 30px;
    margin-top: 45px;
    min-width: unset;
    height: fit-content;
    width: 40%;
  }

  @media (max-width: 560px) {
    margin-bottom: 15px;
    margin-left: 15px;
    margin-top: 60px;
  }
}
</style>