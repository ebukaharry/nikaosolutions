<template>
  <section class="p-4 pt-12 md:pt-0 md:m-4 md:mx-16 xl:mx-36">
    <div class="text-center">
      <h1 class="md:text-lg font-800 uppercase pb-5">We are NikaoSolutions</h1>
      <p class="lg:max-w-[50%] mx-auto text-lg lg:text-2xl">
        Collaborating with international brands, founders, start-ups, venture capitals, and more –
        producing, results-driven, unique products and experiences from conception to delivery.
      </p>
    </div>
    <!-- <div class="my-8">
            <Marquee class="font-800">Great Ideas, Great Designs, Every Media Solution.</Marquee>
            
        </div> -->
    <div class="flex brands gap-4 my-12 object-contain overflow-hidden">
      <img
        src="../assets/images/brand-1.png
            "
        alt=""
        class="aspect-[4/3] w-[15%]"
      />
      <img src="../assets/images/brand-2.png" alt="" class="aspect-[4/3] w-[15%]" />
      <img src="../assets/images/brand-3.png" alt="" class="aspect-[4/3] w-[15%]" />
      <img src="../assets/images/brand-4.png" alt="" class="aspect-[4/3] w-[15%]" />
      <img
        src="../assets/images/brand-5.jpg"
        alt=""
        class="aspect-[4/3] w-[15%] mix-blend-color-burn"
      />
      <img src="../assets/images/brand-6.png" alt="" class="aspect-[4/3] w-[15%]" />
    </div>
  </section>
</template>
<script>
import Marquee from './Marquee.vue'
export default {
  name: 'MainContent',
  components: {
    Marquee
  }
}
</script>
<style></style>
