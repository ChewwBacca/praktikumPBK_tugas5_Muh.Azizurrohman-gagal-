<template>
  <div id="app">
    <Header />
    <HeroSection />
    <FeaturedProducts />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import HeroSection from './components/HeroSection.vue';
import FeaturedProducts from './components/FeaturedProducts.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    HeroSection,
    FeaturedProducts,
    Footer
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

body {
  font-family: 'Roboto', sans-serif;
  margin: 0;
  padding: 0;
}

#app {
  text-align: center;
}
</style>
