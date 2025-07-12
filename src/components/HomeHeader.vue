<template>
    <div
    class="bg-[url('@/assets/Header_Image.svg')] bg-no-repeat bg-center bg-cover aspect-[28/17] bg-[#2e1893d9] bg-blend-lighten flex flex-col items-center"
    >
        <div class="flex justify-center pt-21 gap-11">
            <a href="" class="text-lg font-medium">Home</a>
            <a href="" class="text-lg font-medium">Features</a>
            <a href="" class="text-lg font-medium">Pricing</a>
            <a href="" class="text-lg font-medium">Blog</a>
            <a href="" class="text-lg font-medium">
                <font-awesome-icon icon="fa-solid fa-basketball" class="text-lg" />
            </a>
            <a href="" class="text-lg">
                <font-awesome-icon icon="fa-brands fa-behance" class="text-lg" />
            </a>
        </div>
        <h3 class="text-xl font-bold pt-35">Startup 3</h3>
        <p class="text-7xl font-bold pt-7">Forget About Code</p>
        <p class="w-184 text-center pt-7 pb-28 text-[22px]">
            Startup Framework gives you complete freedom over your creative process — you don’t have to
            think about any technical aspects. There are no limits and absolutely no coding.
        </p>
        <button class="bg-[#482be7] px-9 py-4 rounded-[100px] hover:bg-blue-500 transition duration-400 ease-in-out cursor-pointer">
            Create an Account
        </button>
    </div>
</template>

<script setup lang="ts">
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
</script>
