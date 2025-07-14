<template>
    <div class="bg-[url('@/assets/Header_Image.svg')] bg-no-repeat bg-center bg-cover aspect-[28/17] bg-[#2e1893d9] bg-blend-lighten flex flex-col items-center justify-around lg:justify-start">
        <div class="card sm:hidden absolute left-0 top-0">
            <Menubar :model="items" class=" bg-amber-50"/>
        </div>
        <div class="hidden sm:flex justify-center items-center lg:pt-21 gap-11">
            <a href="" class="text-base lg:text-lg font-medium" @click.prevent="">Home</a>
            <a href="" class="text-base lg:text-lg font-medium" @click.prevent="scrollToSection('featuresSection')">Features</a>
            <a href="" class="text-base lg:text-lg font-medium" @click.prevent="scrollToSection('pricingSection')">Pricing</a>
            <a href="" class="text-base lg:text-lg font-medium" @click.prevent="">Blog</a>
            <a href="" class="text-base lg:text-lg font-medium" @click.prevent="">
                <font-awesome-icon icon="fa-solid fa-basketball" class="text-base lg:text-lg" />
            </a>
            <a href="" class="text-base lg:text-lg" @click.prevent="">
                <font-awesome-icon icon="fa-brands fa-behance" class="text-base lg:text-lg" />
            </a>
        </div>
        <h3 class="text-base lg:text-lg font-bold lg:pt-35">Startup 3</h3>
        <p class="text-3xl sm:text-6xl lg:text-7xl font-bold lg:pt-7">Forget About Code</p>
        <p class="px-5 md:px-0 md:w-184 text-center lg:pt-7 lg:pb-14 xl:pb-28 text-xs sm:text-lg lg:text-[22px]">
            Startup Framework gives you complete freedom over your creative process — you don’t have to
            think about any technical aspects. There are no limits and absolutely no coding.
        </p>
        <button class="bg-[#482be7] px-2 sm:px-5 lg:px-9 py-2 sm:py-3 lg:py-4 rounded-[100px] hover:bg-blue-500 transition duration-400 ease-in-out cursor-pointer">
            <p class="text-xs sm:text-lg font-medium">Create an Account</p>
        </button>
    </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Menubar from "primevue/menubar";

const scrollToSection = (id: string) => {
    const el = document.getElementById(id);
    if (el) {
      el.scrollIntoView({ behavior: 'smooth' });
    }
}

const items = ref([
    {
        label: 'Home',
    },
    {
        label: 'Features',
        command: () => {
            scrollToSection('featuresSection');
        }
    },
    {
        label: 'Pricing',
        command: () => {
            scrollToSection('pricingSection');
        }
    },
    {
        label: 'Blog',
    },
    {
        label: 'Dribble',
    },
    {
        label: 'Behance',
    },
    ]);

</script>

<style scoped>
:deep(.p-menubar) {
    background: transparent !important;
    border: none !important;
    box-shadow: none !important;
    width: 200px;
}
</style>