<template>
  <section>
    <div class="hero absolute top-[30%] md:top-[35%] left-[10%]">
      <p class="text-slate-600 font-600 hidden md:block text-xs md:ml-2">We are</p>
      <h2 class="text-[#B7A996] font-600 text-5xl md:text-8xl pb-3">
        Unleashing Creativity,<br />Powering Technology
      </h2>
      <p class="text-slate-600 font-600 text-xs md:text-lg">
        Take your business to a new level <br />
        with our services.
      </p>
      <div class="cta mt-12 mx-auto justify-center">
        <Button
          text="Get started"
          :class="[
            'text-[#B7A996] md:py-[.9rem] md:px-[3rem] text-base md:text-xl hover:bg-[#746a5dca] hover:text-white'
          ]"
        />
      </div>
      <i
        class="fa-solid fa-angles-down fa-beat-fade text-[#B7A99] flex justify-center relative top-[10rem] left-[-5%] xl:left-[10rem] text-base md:text-3xl cursor-pointer"
      ></i>
    </div>
    <img
      class="hero min-h-[100vh] object-cover"
      src="../assets/images/laptop-bg.jpg"
      alt="background"
    />
    <!-- <div class="absolute inset-0 bg-gray-800 opacity-60"></div> -->
  </section>
</template>
<script>
import Button from './Button.vue'
export default {
  name: 'Hero',
  components: {
    Button
  }
}
</script>
<style>
h2 {
  background: -webkit-linear-gradient(#eee, #333);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
