<template>
    <div
    class="bg-[url('@/assets/Contact_Image.svg')] bg-no-repeat bg-center bg-cover aspect-[1440/770] bg-[#2e189378] bg-blend-lighten flex items-center justify-center gap-22.5"
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
        <div class="bg-white rounded-[10px] pt-14.5 px-12.5 flex flex-col items-center ">
            <div class="flex justify-center items-center gap-7.5">
                <div>
                    <p class="text-[#1e0e62] text-sm pb-1.5 font-bold tracking-widest">YOUR NAME</p>
                    <input 
                        type="text" 
                        placeholder="First name" 
                        class="outline-[#ebeaed] outline-2 rounded-4xl w-50 h-12 placeholder:text-[#15143966]  focus:outline-stone-400 text-lg text-[#15143966] pl-6"
                    >
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
              <div class="w-full pt-8.5">
                <p class="text-[#1e0e62] text-sm pb-1.5 font-bold tracking-widest">INPUT FIELD</p>
                <input 
                    type="email" 
                    placeholder="name@mail.com" 
                    class="outline-[#ebeaed] outline-2 rounded-4xl w-full h-12 placeholder:text-[#15143966]  focus:outline-stone-400 text-lg text-[#15143966] pl-6"
                >
                </div>
                <div class="w-full pt-8.5">
                    <p class="text-[#1e0e62] text-sm pb-1.5 font-bold tracking-widest">YOUR MESSAGE</p>
                    <textarea placeholder="Message" class="outline-[#ebeaed] outline-2 rounded-[10px] w-full h-28 placeholder:text-[#15143966]  focus:outline-stone-400 text-lg text-[#15143966] px-5 py-3 resize-none"/>
                </div>
                <div class="flex justify-between items-center w-full pt-7 pb-14">
                  <label class="flex items-center space-x-2 cursor-pointer gap-3">
                        <input type="checkbox" class="form-checkbox h-5 w-5 text-amber-500 accent-[#25dac5] rounded-4xl cursor-pointer"/>
                            <span class="text-[#15143966] text-base font-normal">Send me a copy</span>
                    </label>
                 <button 
                    class="bg-[#25dac5] rounded-[100px] px-9.5 py-3 hover:bg-teal-300 transition duration-400 ease-in-out cursor-pointer">
                    <p class="text-xl font-medium">Send</p>
                </button>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
</script>