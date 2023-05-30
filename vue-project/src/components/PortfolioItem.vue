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
  <div class="card" style="width: 18rem;">
  <img :src="imageUrl" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">{{ title }}</h5>
    <p class="card-text">{{ abstract }}.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
  <!-- <div class="custom-component"></div>
  <div class="title text-center"  :style="{backgroundColor: color}">
    <img :src="imageUrl" alt="" class="image image-fuid">
    <h2>{{ title }}</h2>
    <p class="abstract">
      {{ abstract }}
    </p>
  </div> -->
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