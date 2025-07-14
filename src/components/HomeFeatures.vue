<template>
    <div
    class="bg-[url('@/assets/Features_Image.svg')] bg-no-repeat bg-center bg-cover aspect-[19/10] bg-[#2e1893d9] bg-blend-lighten flex items-center"
    id="featuresSection"
    >
      <img src="@/assets/Laptop.svg" alt="" class="hidden md:block h-[70%]">
      <div class="flex flex-col p-5 lg:pl-14">
        <h3 class="text-4xl lg:text-[42px] font-bold text-center md:text-left">We Create Something New</h3>
        <p class="text-lg lg:text-[22px] font-medium lg:w-150 pt-5 text-center md:text-left">
            We have created a new product that will help designers, developers and companies create websites for their startups quickly and easily.
        </p>
        <div class="flex justify-center md:justify-start gap-8">
            <div class="pt-16 flex flex-col items-center md:items-start">
                <font-awesome-icon icon="fa-regular fa-clone" class="text-4xl self mx-auto"/>
                <h4 class="text-xs lg:text-sm font-bold pt-7 ">30 NEW FEATURE PAGES</h4>
                <p class="w-67 text-sm lg:text-base font-normal pt-4 text-wrap text-center md:text-left">
                    Startup Framework contains components and complex blocks which can easily. 
                </p>
            </div>
            <div class="pt-16 flex flex-col items-center md:items-start">
               <font-awesome-icon icon="fa-regular fa-gem" class="text-4xl"/>
                <h4 class="text-xs lg:text-sm font-bold pt-7">USEFUL SYMBOL COMPONENTS</h4>
                <p class="w-67 text-sm lg:text-base font-normal pt-4 text-wrap text-center md:text-left">
                    Samples will show you the feeling on how to play around using the components. 
                </p>
            </div>
        </div>
      </div>
    </div>
</template>

<script setup lang="ts">
</script>