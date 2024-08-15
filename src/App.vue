<script>
import Hero from './components/Hero.vue'
import Header from './components/Header.vue'
export default {
  name: 'App',
  components: {
    Header,
    Hero,
  }
}
</script>

<template>
  <main >
    <Hero />
    <Header class="p-4 md:m-4 md:mx-36"/>
  </main>
</template>

<style scoped></style>
