<template>
    <section></section>
    <section>
        <div class="hero absolute top-[30%] md:top-[35%] left-[10%]">
            <p class="text-slate-600 font-600 hidden md:block text-xs md:ml-2">We are</p>
            <h2 class="text-slate-600 font-600 text-5xl md:text-8xl text-gray-4  invert">Unleashing Creativity,<br>Powering Technology</h2>
            <p class="text-slate-600 font-600 text-xs md:text-lg mt-3 md:mt-4">Take your business to a new level <br> with our services.</p>
            <div class="cta mt-12 mx-auto justify-center">
                <Button text="Get started" :class="['text-slate-500 invert md:py-[.9rem] md:px-[3rem] text-base md:text-xl']"/>
            </div>
        </div>
        <img class="hero min-h-[100vh] object-cover" src="../assets/images/laptop-bg.jpg" alt="background">
    <!-- <div class="absolute inset-0 bg-gray-800 opacity-60"></div> -->

    </section>
</template>
<script>
import Button from './Button.vue'
export default {
    name: 'Hero',
    components: {
        Button,
    },
}
</script>
<style scoped>
</style>