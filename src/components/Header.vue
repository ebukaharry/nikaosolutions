<template>
  <nav class="navbar md:bg-transparent bg-white md:flex md:justify-between" :class="[isMenuOpen ? 'bg-white' : 'bg-[transparent]']">
    <div class="flex justify-between items-center">
      <a href="#" class="text-gray-800 text-2xl w-[80px]"><img src="../assets/images/logo.png" alt=""></a>
      <button class="md:hidden" :class="[isMenuOpen ? 'text-slate-500 invert' : 'text-white']" @click="toggleMenu">menu</button>
    </div>
    <div :class="['mt-28 md:mt-0 flex flex-col h-[100vh] md:h-auto md:flex-rw md:justify-between', { block: isMenuOpen, hidden: !isMenuOpen }]" class="md:block">
      <ul class="md:flex space-y-4 md:space-y-0 md:space-x-6 p-4">
        <p class="text-gray-600 invert md:hidden">Menu</p>
        <li v-for="link in navLinks" :key="link.text" class="md:text-white text-gray-800">
          <a :href="link.href" class="hover:underline hover:underline-offset-4 hover:decoration-2 font-400 font-lighter text-4xl md:text-sm md:capitalize">{{ link.text }}</a>
        </li>
        <li><Button text="Get Started" link="#" :class="[isMenuOpen ? 'text-gray-800 hover:bg-gray-800 hover:text-white mt-6' : 'text-slate-900 invert']"/></li>

        <div class="get-in-touch pt-32 md:hidden">
            <p class="text-gray-600 invert mb-2">Get in touch</p>
            <a class="underline underline-offset-4 decoration-gray-300 hover:decoration-gray-800" href="mailto:info@nikaosolutions.com">info@nikaosolutions.com</a>
        </div>
      </ul>
    </div>
  </nav>
</template>

<script>
import Button from './Button.vue'
export default {
    components: {
        Button,
    },
  data() {
    return {
      isMenuOpen: false,
      navLinks: [
        { text: 'What we do', href: '#' },
        { text: 'Projects', href: '#' },
        { text: 'Company', href: '#' },
        { text: 'Contacts', href: '#' }
      ]
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
    }
  }
}
</script>

<style scoped>
    .navbar {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
    }
</style>
