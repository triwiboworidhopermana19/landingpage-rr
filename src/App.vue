<script setup lang="ts"></script>

<template>
  <div class="w-full h-screen px-22">
    <section name="header">
      <header class="flex w-full justify-between items-center pt-5">
        <h1 class="font-semibold text-4xl font-lobster-two brand-name">Keripik R & R</h1>
        <div class="flex shrink-0 justify-between items-center gap-16">
          <a
            href="#"
            class="relative font-normal text-lg after:absolute after:content-[''] after:w-full after:left-0 after:bottom-0 after:border-solid after:border-b-2 after:border-primary after:rounded-xl"
            >Home</a
          >
          <a href="#" class="relative font-normal text-lg">Menu</a>
          <a href="#" class="relative font-normal text-lg">Service</a>
        </div>
        <div class="flex items-center gap-4">
          <button
            class="w-[100px] h-[38px] rounded-lg bg-primary text-white font-semibold cursor-pointer hover:bg-secondary"
          >
            Register
          </button>
          <button
            class="w-[100px] h-[38px] border border-solid border-primary rounded-lg bg-transparent text-primary font-semibold cursor-pointer hover:bg-secondary hover:border-0 hover:text-white"
          >
            Login
          </button>
        </div>
      </header>
    </section>
    <section name="hero" class="w-full relative overflow-hidden">
      <div class="w-full flex justify-between items-center">
        <!-- Left Content -->
        <div class="w-[45%] mt-10">
          <div class="space-y-2">
            <h1 class="text-5xl font-bold">
              <span class="text-secondary">Meat , Eat & Enjoy</span><br />
              <span class="text-black">the true taste</span>
            </h1>
            <p class="font-normal text-lg max-w-[467px]">
              Lorem ipsum dolor sit amet consectetur. Maecenas nunc amet sollicitudin odio purus
              dictumst mauris enim
            </p>
          </div>

          <button
            class="flex items-center justify-center gap-3 w-[201px] h-[53px] mt-8 bg-primary hover:bg-secondary text-white rounded-xl font-semibold"
          >
            <div>SEE MORE</div>
            <svg
              width="10"
              height="16"
              viewBox="0 0 10 16"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M9.65934 8.84973L3.07618 15.6476C2.62116 16.1175 1.8854 16.1175 1.43523 15.6476L0.34126 14.518C-0.113753 14.0481 -0.113753 13.2883 0.34126 12.8235L5.00756 8.005L0.34126 3.1865C-0.113753 2.71665 -0.113753 1.95689 0.34126 1.49203L1.43039 0.35239C1.8854 -0.117463 2.62116 -0.117463 3.07134 0.35239L9.6545 7.15027C10.1144 7.62012 10.1144 8.37988 9.65934 8.84973Z"
                fill="white"
              />
            </svg>
          </button>

          <!-- Search bar -->
          <div
            class="flex items-center gap-2 rounded-full px-4 py-2 shadow-md w-full max-w-md mt-6"
          >
            <input type="text" placeholder="Search Food..." class="flex-1 outline-none text-sm" />
            <button>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="w-5 h-5 text-gray-500"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M12 4v16m8-8H4"
                />
              </svg>
            </button>
          </div>

          <!-- Social icons -->
          <div class="flex gap-4 mt-4">
            <i class="fab fa-instagram text-xl text-gray-500"></i>
            <i class="fab fa-facebook text-xl text-gray-500"></i>
            <i class="fab fa-twitter text-xl text-gray-500"></i>
          </div>
        </div>

        <!-- Right Content -->
        <div class="w-[55%] relative">
          <img src="/carousel-1.png" class="w-full max-w-[500px] mx-auto z-10" alt="Main Food" />
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="css" scoped>
header .brand-name {
  background: linear-gradient(to bottom, #f4d61b 0%, #f47217 55%, #da0d0f 75%);
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
  -webkit-text-fill-color: transparent;
}
</style>

<style lang="css">
@reference 'tailwindcss';

#app {
  @apply max-w-[1440px] m-auto;
}
</style>
