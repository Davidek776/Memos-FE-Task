<template>
    <div class="bg-[#2f1893] flex flex-col items-center justify-center py-25" id="pricingSection">
        <h1 class="text-2xl sm:text-4xl lg:text-[42px] font-bold ">Plans & Pricing</h1>
        <p class="text-base sm:text-lg lg:text-[22px] font-medium sm:w-146 pt-7.5 text-center px-5 sm:px-0">
            Startup Framework is free forever — you only pay for custom domain hosting or to export your site.
        </p>
        <div class="hidden md:flex w-full gap-7.5 justify-center pt-13.5 ">
            <Pricing-plan-list :pricingPlan="starterPlan"/>
            <Pricing-plan-list :pricingPlan="profesionalPlan">
                <button class="bg-[#e93a7d] rounded-[100px] px-10 lg:px-15 py-3 lg:py-4 hover:bg-[#fa7bac] transition duration-400 ease-in-out cursor-pointer">
                    <p class="text-lg lg:text-xl font-medium">Get Started</p>
                </button>
            </Pricing-plan-list>
            <Pricing-plan-list :pricingPlan="teamPlan"/>
        </div>
        <Pricing-carousel 
            :pricingPlans="allPricingPlans"
            class="md:hidden" 
        />
    </div>
</template>

<script setup lang="ts">
import PricingPlanList from './home-pricing-components/PricingPlanList.vue'
import PricingCarousel from './home-pricing-components/PricingCarousel.vue'

export type PricingPlanItem = {
    name: string
    isIncluded: boolean
}

export type PricingPlan = {
    type: string,
    price: number,
    items: PricingPlanItem[]
}

const starterPlan: PricingPlan = {
    type: "Starter",
    price: 9.99,
    items: [
    {
        name: '2 GB of space',
        isIncluded: true
    },
    {
        name: '14 days of backups',
        isIncluded: true
    },
    {
        name: 'Social integrations',
        isIncluded: true
    },
    {
        name: 'Client billing',
        isIncluded: true
    },
    {
        name: 'Remote access',
        isIncluded: false
    },
    {
        name: 'Custom domain',
        isIncluded: false
    },
    {
        name: '24 hours support',
        isIncluded: false
    },
    {
        name: 'Admin tools',
        isIncluded: false
    },
    {
        name: 'Colaboration tools',
        isIncluded: false
    },
    {
        name: 'User management',
        isIncluded: false
    }
]
}

const profesionalPlan: PricingPlan = {
    type: "Professional",
    price: 19.99,
    items: [
    {
        name: '2 GB of space',
        isIncluded: true
    },
    {
        name: '14 days of backups',
        isIncluded: true
    },
    {
        name: 'Social integrations',
        isIncluded: true
    },
    {
        name: 'Client billing',
        isIncluded: true
    },
    {
        name: 'Remote access',
        isIncluded: true
    },
    {
        name: 'Custom domain',
        isIncluded: true
    },
    {
        name: '24 hours support',
        isIncluded: true
    },
    {
        name: 'Admin tools',
        isIncluded: false
    },
    {
        name: 'Colaboration tools',
        isIncluded: false
    },
    {
        name: 'User management',
        isIncluded: false
    }
]
}

const teamPlan: PricingPlan = {
    type: "Team",
    price: 49.99,
    items:[
    {
        name: '2 GB of space',
        isIncluded: true
    },
    {
        name: '14 days of backups',
        isIncluded: true
    },
    {
        name: 'Social integrations',
        isIncluded: true
    },
    {
        name: 'Client billing',
        isIncluded: true
    },
    {
        name: 'Remote access',
        isIncluded: true
    },
    {
        name: 'Custom domain',
        isIncluded: true
    },
    {
        name: '24 hours support',
        isIncluded: true
    },
    {
        name: 'Admin tools',
        isIncluded: true
    },
    {
        name: 'Colaboration tools',
        isIncluded: true
    },
    {
        name: 'User management',
        isIncluded: true
    }
]
}

const allPricingPlans = [starterPlan, profesionalPlan, teamPlan]
</script>