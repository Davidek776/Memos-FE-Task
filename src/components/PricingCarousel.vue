<template>
    <div class="w-full pt-13.5 px-0 sm:px-10">
        <Carousel 
            :value="pricingPlans" 
            :numVisible="1" 
            :numScroll="1" 
            :showIndicators="true"
            :showNavigators="true"
            :circular="true"
            :autoplayInterval="5000"
        >
            <template #item="slotProps">
                <div class="flex justify-center px-4">
                    <Pricing-plan-list 
                        :pricingPlan="slotProps.data"
                    >
                        <button 
                            v-if="slotProps.data.type === 'Professional'"
                            class="bg-[#e93a7d] rounded-[100px] px-5 sm:px-10 lg:px-15 py-2 sm:py-3 lg:py-4 hover:bg-[#fa7bac] transition duration-400 ease-in-out cursor-pointer"
                        >
                            <p class="text-lg lg:text-xl font-medium">Get Started</p>
                        </button>
                    </Pricing-plan-list>
                </div>
            </template>
        </Carousel>
    </div>
</template>

<script setup lang="ts">
import Carousel from 'primevue/carousel'; 
import PricingPlanList from './PricingPlanList.vue';
import type { PricingPlan } from './HomePricing.vue';

defineProps<{
    pricingPlans: PricingPlan[]
}>()
</script>