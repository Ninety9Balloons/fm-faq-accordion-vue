<script setup>
import Main from "./components/Main.vue";
</script>

<template>
    <div class="container relative bg-light-pink w-screen h-full mx-auto">
        <div
            class="container min-h-screen mx-auto relative flex flex-col justify-center items-center bg-light-pink py-10"
        >
            <img
                class="absolute z-10 inset-x-0 top-0 w-full object-cover max-h-60 md:h-60 sm:block md:hidden"
                src="./assets/images/background-pattern-mobile.svg"
            />
            <img
                class="absolute z-10 inset-x-0 top-0 w-full object-cover max-h-60 md:h-60 sm: hidden md:block"
                src="./assets/images/background-pattern-desktop.svg"
            />
            <Main
                class="z-20 relative bg-white max-w-xs mx-auto rounded-xl p-4 md:max-w-xl"
            />
        </div>

        <div class="attribution mt-4 mb-4 absolute inset-x-0 bottom-0">
            Challenge by
            <a
                href="https://www.frontendmentor.io?ref=challenge"
                target="_blank"
                >Frontend Mentor</a
            >. Coded by <a href="#">Troy Reuther</a>.
        </div>
    </div>
</template>

<style scoped>
.attribution {
    font-size: 11px;
    text-align: center;
}
.attribution a {
    color: hsl(228, 45%, 44%);
}
</style>
