<script>
import Hero from './components/Hero.vue'
import Header from './components/Header.vue'
import MainContent from './components/MainContent.vue'
export default {
  name: 'App',
  components: {
    Header,
    Hero,
    MainContent
  }
}
</script>

<template>
  <main>
    <Hero />
    <Header class="p-4 md:m-4 md:mx-16 xl:mx-36" />
    <MainContent class="p-4 md:m-4 md:mx-16 xl:mx-36" />
  </main>
</template>

<style scoped></style>
