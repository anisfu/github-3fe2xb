<template>
  <div class="relative bg-[#d9ebd8]">
  <div class="mx-auto max-w-7xl px-6">
    <div class="flex items-center justify-between border-b-2 border-gray-100 py-6 md:justify-start md:space-x-10">
      <div class="flex justify-start lg:w-0 lg:flex-1">
        <a href="/">
          <span class="sr-only"></span>
          <img class="h-8 w-auto sm:h-10" src="https://tailwindui.com/img/logos/mark.svg?color=gray&shade=500" alt="logo-app">
        </a>
      </div>
      <div class="-my-2 -mr-2 md:hidden">
        <button type="button" class="inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500" aria-expanded="false" @click="openMenu">
          <span class="sr-only">Open menu</span>
          <!-- Heroicon name: outline/bars-3 -->
          <svg class="h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
          </svg>
        </button>
      </div>
      <nav class="hidden space-x-10 md:flex">
        <a href="https://birthday-calculator-en.vercel.app/" target="_blank" class="text-base font-medium text-gray-500 hover:text-gray-900">Birthday Calculator</a>
        <a href="https://calculator-home.vercel.app/" class="text-base font-medium text-gray-500 hover:text-gray-900">Famous Birthdays</a>
        <!-- <a href="#" class="text-base font-medium text-gray-500 hover:text-gray-900">How Old I Will be?</a> -->
      </nav>
      <!-- <div class="hidden items-center justify-end md:flex md:flex-1 lg:w-0">
        <a href="#" class="ml-8 inline-flex items-center justify-center whitespace-nowrap rounded-md border border-transparent bg-indigo-600 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700">Sign up</a>
      </div> -->
    </div>
  </div>

  <!--
    Mobile menu, show/hide based on mobile menu state.
    Entering: "duration-200 ease-out"
      From: "opacity-0 scale-95"
      To: "opacity-100 scale-100"
    Leaving: "duration-100 ease-in"
      From: "opacity-100 scale-100"
      To: "opacity-0 scale-95"
  -->
  <div class="absolute inset-x-0 top-0 origin-top-right transform p-2 transition" v-if="isCollapse">
    <div class="divide-y-2 divide-gray-50 rounded-lg bg-white shadow-lg ring-1 ring-black ring-opacity-5">
      <div class="px-5 pt-5 pb-6">
        <div class="flex items-center justify-between">
          <div>
            <img class="h-8 w-auto" src="https://tailwindui.com/img/logos/mark.svg?color=gray&shade=500" alt="Your Company">
          </div>
          <div class="-mr-2">
            <button type="button" class="inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500" @click="closeMenu">
              <span class="sr-only">Close menu</span>
              <!-- Heroicon name: outline/x-mark -->
              <svg class="h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
              </svg>
            </button>
          </div>
        </div>
        <div class="mt-6">
          <nav class="grid gap-y-8">
            <a href="https://birthday-calculator-en.vercel.app/" target="_blank" class="-m-3 flex items-center rounded-md p-3 hover:bg-gray-50">
              <!-- Heroicon name: outline/shield-check -->
              <svg class="h-6 w-6 flex-shrink-0 text-gray-500" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9 12.75L11.25 15 15 9.75m-3-7.036A11.959 11.959 0 013.598 6 11.99 11.99 0 003 9.749c0 5.592 3.824 10.29 9 11.623 5.176-1.332 9-6.03 9-11.622 0-1.31-.21-2.571-.598-3.751h-.152c-3.196 0-6.1-1.248-8.25-3.285z" />
              </svg>
              <span class="ml-3 text-base font-medium text-gray-900">Birthday Calculator</span>
            </a>

            <a href="#" class="-m-3 flex items-center rounded-md p-3 hover:bg-gray-50">
              <!-- Heroicon name: outline/squares-2x2 -->
              <svg class="h-6 w-6 flex-shrink-0 text-gray-500" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6A2.25 2.25 0 016 3.75h2.25A2.25 2.25 0 0110.5 6v2.25a2.25 2.25 0 01-2.25 2.25H6a2.25 2.25 0 01-2.25-2.25V6zM3.75 15.75A2.25 2.25 0 016 13.5h2.25a2.25 2.25 0 012.25 2.25V18a2.25 2.25 0 01-2.25 2.25H6A2.25 2.25 0 013.75 18v-2.25zM13.5 6a2.25 2.25 0 012.25-2.25H18A2.25 2.25 0 0120.25 6v2.25A2.25 2.25 0 0118 10.5h-2.25a2.25 2.25 0 01-2.25-2.25V6zM13.5 15.75a2.25 2.25 0 012.25-2.25H18a2.25 2.25 0 012.25 2.25V18A2.25 2.25 0 0118 20.25h-2.25A2.25 2.25 0 0113.5 18v-2.25z" />
              </svg>
              <span class="ml-3 text-base font-medium text-gray-900">Famous Birthday</span>
            </a>

            <a href="#" class="-m-3 flex items-center rounded-md p-3 hover:bg-gray-50">
              <!-- Heroicon name: outline/arrow-path -->
              <svg class="h-6 w-6 flex-shrink-0 text-gray-500" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                <path stroke-linecap="round" stroke-linejoin="round" d="M16.023 9.348h4.992v-.001M2.985 19.644v-4.992m0 0h4.992m-4.993 0l3.181 3.183a8.25 8.25 0 0013.803-3.7M4.031 9.865a8.25 8.25 0 0113.803-3.7l3.181 3.182m0-4.991v4.99" />
              </svg>
              <span class="ml-3 text-base font-medium text-gray-900">How Old Will I Be?</span>
            </a>
          </nav>
        </div>
      </div>
    </div>
  </div>
</div>

</template>

<script>
export default{
  data() {
    return {
      isCollapse: false
    }
  },
  methods: {
    openMenu() {
      this.isCollapse = true;
    },
    closeMenu() {
      this.isCollapse = false;
    }
  }
}
</script>