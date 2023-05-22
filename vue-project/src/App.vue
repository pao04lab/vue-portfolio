<script >
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import PortfolioItem from './components/PortfolioItem.vue'
import worksData from './assets/works.json'

export default {
  data() {
    return {
      works: worksData,
    };
  },
  components: {
    PortfolioItem,
  },
};



</script>

<template>
  <header class="mb-4">
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
    <div class="wrapper">
      <HelloWorld msg="custom message" />
    </div>
  </header>

  <main>
    <div class="row">
      <div class="col">
        <PortfolioItem 
          title="ciao mondo"
          abstract="Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore."
          imageUrl="/images/pere.jpg"
          />
      </div>
      <div class="col">
        <PortfolioItem 
          title="Ola"
          abstract="Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore. magna aliqua."
          imageUrl="https://source.unsplash.com/random/?green" />
      </div>
    </div>
  </main>

  <div id="works">
    <p v-for="work in works" :key="work.id">
      <h1>{{ work.title }}</h1>
      <p class="description">
        {{ work.description }}
      </p>
      <img  :src="work.image_detail" width="125" height="125" />
    </p>
  </div>
</template>

<style scoped>


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