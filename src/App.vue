<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Navigation from './components/Navigation.vue';
import Footer from './components/Footer.vue';
import axios from "axios";
</script>

<template>
  <Navigation msg="You did it!" />
  <main>
    <RouterView />
  </main>
  <Footer />
</template>

<style scoped>
main {
  display: block;
  margin: 0 auto;
  max-width: 1200px;
  padding: 0 20px;
  h1{
    font-size: 30vh;
  }
}
</style>
