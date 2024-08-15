<template>
  <nav class="md:bg-transparent bg-white md:flex md:justify-between">
    <div class="flex justify-between items-center">
      <a href="#" class="text-gray-800 text-2xl font-bold w-[80px]"><img src="../assets/images/logo.png" alt=""></a>
      <button class="text-gray-800 md:hidden" @click="toggleMenu">menu</button>
    </div>
    <div :class="['mt-28 md:mt-0 flex flex-col h-[100vh] md:h-auto md:flex-rw md:justify-between', { block: isMenuOpen, hidden: !isMenuOpen }]" class="md:block">
      <ul class="md:flex space-y-4 md:space-y-0 md:space-x-6 p-4">
        <p class="text-gray-400 md:hidden">Menu</p>
        <li v-for="link in navLinks" :key="link.text" class="text-gray-800 ">
          <a :href="link.href" class="hover:underline hover:underline-offset-4 hover:decoration-2 font-400 text-4xl md:text-sm md:capitalize">{{ link.text }}</a>
        </li>

        <div class="get-in-touch pt-32 md:hidden">
            <p class="text-gray-400 mb-2">Get in touch</p>
            <a class="underline underline-offset-4 decoration-gray-300" href="mailto:info@nikaosolutions.com">info@nikaosolutions.com</a>
        </div>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
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
/* Additional custom styles can be added here if needed */
</style>
