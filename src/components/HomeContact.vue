<template>
  <div
    class="bg-[url('@/assets/Contact_Image.svg')] bg-no-repeat bg-center bg-cover aspect-[1440/770] bg-[#2e189378] bg-blend-lighten flex-col lg:flex-row lg:flex items-center justify-center gap-22.5 py-10 lg:py-0"
  >
    <div class="flex justify-center">
      <div class="flex flex-col items-start lg:items-center lg:block pb-16 lg:pb-0 px-5 sm:px-0">
        <h2 class="text-lg sm:text-4xl lg:text-[42px] font-bold">Let’s Keep in Touch</h2>
        <p class="text-base sm:text-lg lg:text-[22px]font-medium sm:w-100 pt-7">
          We have created a new product that will help designers, developers and companies create
          websites for their startups quickly and easily.
        </p>
        <a href="tel:15555055050" class="flex items-center text-base sm:text-lg gap-4 pt-13">
          <font-awesome-icon icon="fa-solid fa-phone text-base text-base lg:text-lg" />
          <p class="text-sm lg:text-base">+1 555 505 5050</p>
        </a>
        <a
          href="mailto:info@designmodo.com"
          class="flex items-center text-sm sm:text-base lg:text-lg gap-4 pt-8"
        >
          <font-awesome-icon icon="fa-solid fa-envelope text-lg" />
          <p class="text-sm lg:text-base">info@designmodo.com</p>
        </a>
        <a href="" class="flex text-lg gap-4 pt-8">
          <font-awesome-icon icon="fa-regular fa-building text-base lg:text-lg" />
          <p class="text-sm lg:text-base">
            San Francisco, CA560 Bush St & <br />20th Ave, Apt5 San Francisco, <br />
            230909
          </p>
        </a>
      </div>
    </div>
    <div class="flex justify-center">
      <div class="bg-white rounded-[10px] pt-14.5 px-12.5 flex flex-col items-center w-120 lg:w-auto">
        <div class="flex justify-center items-baseline gap-7.5 w-full">
          <div>
            <p class="text-[#1e0e62] text-xs md:text-sm pb-1.5 font-bold tracking-widest">
              YOUR NAME
            </p>
            <input
              type="text"
              placeholder="First name"
              v-model="form.name"
              class="outline-[#ebeaed] outline-2 rounded-4xl w-full sm:w-50 h-12 placeholder:text-[#15143966] focus:outline-stone-400 text-lg text-[#15143966] text-center sm:text-left sm:pl-6"
            />
            <p v-if="v$.form.name.$error" class="text-red-500 text-sm">Name is required.</p>
          </div>
          <div>
            <p class="text-[#1e0e62] text-xs md:text-sm pb-1.5 font-bold tracking-widest">BUDGET</p>
            <select
              v-model="form.budget"
              class="outline-[#ebeaed] outline-2 focus:outline-stone-400 rounded-4xl w-35 h-12 placeholder:text-[#15143966] text-lg text-[#1e0e62] pl-6 border-r-24 border-transparent"
            >
              <option selected>$500</option>
              <option value="$1000">$1000</option>
              <option value="$2000">$2000</option>
              <option value="$5000">$5000</option>
              <option value="$7000">$7000</option>
            </select>
            <p v-if="v$.form.budget.$error" class="text-red-500 text-sm">Budget is required.</p>
          </div>
        </div>
        <div class="w-full pt-8.5">
          <p class="text-[#1e0e62] text-xs md:text-sm pb-1.5 font-bold tracking-widest">
            INPUT FIELD
          </p>
          <input
            type="email"
            placeholder="name@mail.com"
            v-model="form.email"
            class="outline-[#ebeaed] outline-2 rounded-4xl w-full h-12 placeholder:text-[#15143966] focus:outline-stone-400 text-lg text-[#15143966] pl-6"
          />
          <p v-if="v$.form.email.$error" class="text-red-500 text-sm">Valid email is required.</p>
        </div>
        <div class="w-full pt-8.5">
          <p class="text-[#1e0e62] text-xs md:text-sm pb-1.5 font-bold tracking-widest">
            YOUR MESSAGE
          </p>
          <textarea
            placeholder="Message"
            v-model="form.message"
            class="outline-[#ebeaed] outline-2 rounded-[10px] w-full h-28 placeholder:text-[#15143966] focus:outline-stone-400 text-lg text-[#15143966] px-5 py-3 resize-none"
          />
          <p v-if="v$.form.message.$error" class="text-red-500 text-sm">Message is required.</p>
        </div>
        <div class="flex justify-between items-center w-full pt-7 pb-14">
          <label class="flex items-center space-x-2 cursor-pointer gap-3">
            <input
              type="checkbox"
              v-model="form.copy"
              class="h-5 w-5 accent-[#25dac5] rounded-4xl cursor-pointer"
            />
            <span class="text-[#15143966] text-base font-normal">Send me a copy</span>
          </label>
          <button
            @click="submitForm"
            class="bg-[#25dac5] rounded-[100px] px-9.5 py-3 hover:bg-teal-300 transition duration-400 ease-in-out cursor-pointer"
          >
            <p class="text-xl font-medium">Send</p>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { reactive } from "vue";
import useVuelidate from "@vuelidate/core";
import { required, email } from "@vuelidate/validators";

const form = reactive({
  name: "",
  budget: "$500",
  email: "",
  message: "",
  copy: false,
});

const rules = {
  form: {
    name: { required },
    budget: { required },
    email: { required, email },
    message: { required },
    copy: {},
  },
};

const v$ = useVuelidate(rules, { form });

const submitForm = async () => {
  v$.value.$touch();
  if (!v$.value.$invalid) {
    alert("Form Submitted:\n" + JSON.stringify(form, null, 2));

    form.name = "";
    form.budget = "";
    form.email = "";
    form.message = "";
    form.copy = false;

    v$.value.$reset();
  }
};
</script>