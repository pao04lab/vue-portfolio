<script setup>
defineProps({
  title: {
    type: String,
    required: true
  },
  abstract: String,
  color: String,
  imageUrl: String
})
</script>

<template>
  <div class="custom-component"></div>
  <div class="title text-center"  :style="{backgroundColor: color}">
    <img :src="imageUrl" alt="" class="image image-fuid">
    <h2>{{ title }}</h2>
    <p class="abstract">
      {{ abstract }}
    </p>
  </div>
</template>

<style scoped>
  .title {
    font-size: 1em;
  }

 .image {
    width: 100%;
    height: 100%;
  }

 /* .custom-component {
    background-color: v-bind(color);
  }*/
</style>