<template>
    <div class="bg-[#2f1893] flex flex-col items-center justify-center py-25" id="pricingSection">
        <h1 class="text-[42px] font-bold ">Plans & Pricing</h1>
        <p class="text-[22px] font-medium w-146 pt-7.5 text-center">Startup Framework is free forever — you only pay for custom domain hosting or to export your site.</p>
        <div class="flex w-full gap-7.5 justify-center pt-13.5">
            <Pricing-plan-list 
                :pricingPlanItems="starterPlanItems"
                planType="Starter"
                :price="9.99"

            />
            <Pricing-plan-list 
                :pricingPlanItems="profesionalPlanItems"
                planType="Professional"
                :price="19.99"

            >
                <button class="bg-[#e93a7d] rounded-[100px] px-15 py-4 hover:bg-[#fa7bac] transition duration-400 ease-in-out cursor-pointer">
                    <p class="text-xl font-medium">Get Started</p>
                </button>
            </Pricing-plan-list>
            <Pricing-plan-list 
                :pricingPlanItems="teamPlanItems"
                planType="Team"
                :price="49.99"
            />
        </div>
    </div>
   
</template>

<script setup lang="ts">
import PricingPlanList from './PricingPlanList.vue'

export type PricingPlanItem = {
    name: string
    isIncluded: boolean
}

const starterPlanItems: PricingPlanItem[] = [
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

const profesionalPlanItems: PricingPlanItem[] = [
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

const teamPlanItems: PricingPlanItem[] = [
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
</script>