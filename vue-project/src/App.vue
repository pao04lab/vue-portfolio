<script >
import PortfolioItem from './components/PortfolioItem.vue'
import Header from './components/Header.vue'
import worksData from './assets/works.json'

export default {
  data() {
    return {
      works: worksData,
    };
  },
  components: {
    Header,
    PortfolioItem,
  },
};


</script>

<template>

  <main>
    <Header />
    <div class="row">
      <div class="col-12 col-md-6" v-for="work in works" :key="work.id">
        <PortfolioItem 
          :title="work.title"
          :abstract="work.description"
          :imageUrl="work.image_thumbnail"
          />
      </div>
    </div>
  </main>

   <!-- <div id="works">
       <p v-for="work in works" :key="work.id">
        <h1>{{ work.title }}</h1>
       <p class="description">
        {{ work.description }}
       </p>
       <img  :src="work.image_detail" width="125" height="125" />
       </p>
       </div>-->
</template>

<style scoped>

.container {
  border: solid red;
}

header {
  line-height: 1.5;
}
.logo {
  display: block;
  margin: 0 auto 2rem;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }
  .logo {
    margin: 0 2rem 0 0;
  }
  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>