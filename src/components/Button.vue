<template>
    <div class="
        button max-w-max h-max
        flex justify-center rounded-3xl uppercase 
        text-xs py-[.4rem] px-[2rem] 
        tracking-[-.02em] border-[.1rem]
        cursor-pointer"
    >
        <a :href="link">
            {{ text }}
        </a>
    </div>  
</template>

<script>
export default {
    name: "Button-Component",
    props: {
        text: String,
        link: String,
    }
}
</script>

<style scoped>
.button {
    border: .1rem solid;
    transform: translateZ(0);
    transition: background-color .6s cubic-bezier(0.075, 0.82, 0.165, 1), color 0.6s cubic-bezier(0.075, 0.82, 0.165, 1);
}

/* .button:hover, .button:active, .button:focus {
    background-color: #252422;
    color: #fff;
    border: .1rem solid #252422; 
} */
</style>

