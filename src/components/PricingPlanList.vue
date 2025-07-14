<template>
    <div class="flex flex-col items-center border-2 border-[#fff5] rounded-[10px] pt-16 pb-14 px-[5%]">
        <div class="">
            <h3 class="text-[22px] font-medium pb-5">{{ planType }}</h3>
            <p class="text-6xl font-bold inline-flex items-start">9.99 
            <sup class="text-base font-normal p-2">$</sup>
            </p>
            <ul class="pb-7.5">
                <li 
                    v-for="item in pricingPlanItems"
                    :key="item.name"
                    class="flex items-center gap-3.5" 
                >
                    <template v-if="item.isIncluded">
                        <font-awesome-icon :icon="['fas', 'check']" class=" text-green-500"/>
                        <p class="text-base font-normal py-2">{{ item.name }}</p>
                    </template>
                    <template v-else>
                        <p class="text-base font-normal opacity-75 self-center pl-7 py-2">{{ item.name }}</p>
                    </template>
                </li>
            </ul>
            <slot>
                <button class="bg-transparent border-2 border-[#fff5] rounded-[100px] px-15 py-4 hover:bg-[#fff] hover:text-zinc-700 transition duration-400 ease-in-out cursor-pointer">
                    <p class="text-xl font-medium">Get Started</p>
                </button>
            </slot>
        </div>
    </div>
</template>

<script setup lang="ts">
import type { PricingPlanItem } from './HomePricing.vue';

defineProps<{
    planType: string,
    pricingPlanItems: PricingPlanItem[]
}>()

</script>