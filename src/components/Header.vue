<template>
  <nav
    class="navbar md:bg-transparent md:flex md:justify-between"
    :class="[isMenuOpen ? 'bg-white' : 'bg-[transparent]']"
  >
    <div class="flex justify-between items-center">
      <a href="#" class="text-gray-800 text-2xl w-[80px]"
        ><img src="../assets/images/logo.png" alt="Logo"
      /></a>
      <button
        class="md:hidden option"
        :class="[isMenuOpen ? 'text-slate-500 invert' : 'text-white']"
        @click="toggleMenu"
      >
        {{ isMenuOpen ? 'close' : 'menu' }}
      </button>
    </div>
    <!-- Adjust the wrapper div to apply transition only on mobile screens -->
    <div
      :class="[
        'mt-28 md:mt-8 flex flex-col h-screen md:h-auto md:flex-row md:justify-between md:max-h-full md:opacity-100 w-full md:w-auto transition-all duration-500 ease-in',
        { 'max-h-screen opacity-100': isMenuOpen, 'max-h-0 opacity-0': !isMenuOpen }
      ]"
      class="md:block overflow-hidden"
    >
      <ul class="md:flex space-y-4 md:space-y-0 md:space-x-6 p-4 md:p-0">
        <p class="text-gray-600 invert md:hidden">Menu</p>
        <li v-for="link in navLinks" :key="link.text" class="md:text-white text-gray-800">
          <a
            :href="link.href"
            class="hover:underline hover:underline-offset-4 hover:decoration-2 font-400 font-lighter text-4xl md:text-sm md:capitalize"
            >{{ link.text }}</a
          >
        </li>
        <li>
          <Button
            text="Get Started"
            link="#"
            :class="[
              isMenuOpen
                ? 'text-[#B7A996] hover:bg-[#B7A996] hover:text-white mt-6'
                : 'text-slate-900 invert'
            ]"
          />
        </li>

        <div class="get-in-touch pt-32 md:hidden">
          <p class="text-gray-600 invert mb-2">Get in touch</p>
          <a
            class="underline underline-offset-4 decoration-gray-300 hover:decoration-gray-800"
            href="mailto:info@nikaosolutions.com"
            >info@nikaosolutions.com</a
          >
        </div>
      </ul>
    </div>
  </nav>
</template>

<script>
import Button from './Button.vue'
export default {
  components: {
    Button
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
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
}

.menulist {
  transition: all 0.3s ease-in-out;
}

ul,
.option,
li {
  transition: all 0.3s ease-in-out;
}
</style>
