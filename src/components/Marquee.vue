<template>
  <div class="overflow-hidden whitespace-nowrap w-full relative">
    <div
      class="flex justify-start items-center animate-marquee gravitas-font text-5xl"
      :style="marqueeStyle"
    >
      <span class="mr-8 will-change-transform translate-x-0 whitespace-nowrap"><slot></slot></span>
      <span class="mr-8 will-change-transform translate-x-0 whitespace-nowrap"><slot></slot></span>
      <span class="mr-8 will-change-transform translate-x-0 whitespace-nowrap"><slot></slot></span>
      <span class="mr-8 will-change-transform translate-x-0 whitespace-nowrap"><slot></slot></span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    speed: {
      type: Number,
      default: 24 // Speed of the scrolling (lower is faster)
    }
  },
  computed: {
    marqueeStyle() {
      return {
        animationDuration: `${this.speed}s`
      }
    }
  }
}
</script>

<style scoped>
/* @import url('https://fonts.googleapis.com/css2?family=Gravitas+One&display=swap'); */

@keyframes marquee {
  from {
    transform: translateX(0%);
  }
  to {
    transform: translateX(-100%);
  }
}

.animate-marquee {
  animation: marquee linear infinite;
}

/* .gravitas-font {
  font-family: "Gravitas One", serif;
  font-weight: 400;
  font-style: normal;
} */
</style>
