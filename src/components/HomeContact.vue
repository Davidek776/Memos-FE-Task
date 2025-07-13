<template>
    <div
    class="bg-[url('@/assets/Contact_Image.svg')] bg-no-repeat bg-center bg-cover aspect-[1440/770] bg-[#2e189378] bg-blend-lighten flex items-center justify-center"
    >
        <div>
            <h2 class="text-[42px] font-bold">Let’s Keep in Touch</h2>
            <p class="text-[22px] font-medium w-100 pt-7">We have created a new product that will help designers, developers and companies create websites for their startups quickly and easily.</p>
            <a href="tel:15555055050" class="flex text-lg gap-4 pt-13">
                <font-awesome-icon icon="fa-solid fa-phone text-base text-lg" />
                <p class="text-base">+1 555 505 5050</p>
            </a>
            <a href="mailto:info@designmodo.com" class="flex text-lg gap-4 pt-8">
                <font-awesome-icon icon="fa-solid fa-envelope text-lg" />
                <p class="text-base">info@designmodo.com</p>
            </a>
            <a href="" class="flex text-lg gap-4 pt-8">
            <font-awesome-icon icon="fa-regular fa-building text-lg" />
            <p class="text-base">San Francisco, CA560 Bush St & 
                <br>20th Ave, Apt5 San Francisco, 
                <br> 230909
            </p>
        </a>
        </div>
        <div class="bg-white rounded-[10px] h-120 pt-14.5 px-12.5 flex flex-col items-center gap-8.5">
            <div class="flex justify-center items-center gap-7.5">
                <div>
                    <p class="text-[#1e0e62] text-sm pb-1.5 font-bold tracking-widest">YOUR NAME</p>
                    <input type="text" placeholder="First name" class="outline-[#ebeaed] outline-2 rounded-4xl w-50 h-12 placeholder:text-[#15143966]  focus:outline-stone-400 text-lg text-[#15143966] pl-6">
                </div>
                <div>
                    <p class="text-[#1e0e62] text-sm pb-1.5 font-bold tracking-widest">BUDGET</p>
                    <select id="countries" class="outline-[#ebeaed] outline-2 focus:outline-stone-400 rounded-4xl w-35 h-12 placeholder:text-[#15143966] text-lg text-[#1e0e62]  pl-6 border-r-24 border-transparent ">
                        <option selected>$500</option>
                        <option value="$1000">$1000</option>
                        <option value="$2000">$2000</option>
                        <option value="$5000">$5000</option>
                        <option value="$7000">$7000</option>
                     
                    </select>
                </div>
            </div>
              <div class="w-full">
                <p class="text-[#1e0e62] text-sm pb-1.5 font-bold tracking-widest">INPUT FIELD</p>
                <input type="email" placeholder="name@mail.com" class="outline-[#ebeaed] outline-2 rounded-4xl w-full h-12 placeholder:text-[#15143966]  focus:outline-stone-400 text-lg text-[#15143966] pl-6">
                </div>
                <div class="w-full">
                    <p class="text-[#1e0e62] text-sm pb-1.5 font-bold tracking-widest">YOUR MESSAGE</p>
                    <textarea placeholder="Message" class="outline-[#ebeaed] outline-2 rounded-[10px] w-full h-28 placeholder:text-[#15143966]  focus:outline-stone-400 text-lg text-[#15143966] px-5 py-3 resize-none"/>
                </div>
                <div class="flex">
                    <label class="flex items-center cursor-pointer">
                    <input type="checkbox" class="form-checkbox h-5 w-5 checked:bg-amber-300 checked:border-transparent" />
                    <span class="text-gray-700">Send me a copy</span>
                    </label>
                </div>
        </div>
    </div>
</template>

<script setup lang="ts">
</script>