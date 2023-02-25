<template>
  <div class="
      relative
      items-top
      justify-center
      min-h-screen
      bg-gray-100
      sm:items-center
    ">
    <Navbar />
    <div class="flex flex-col px-6 2xl:px-72 xl:px-64 lg:px-40 md:px-20 sm:px-16 py-10">
      <div class="grid grid-cols-1 lg:grid-cols-3 md:grid-cols-3 sm:grid-cols-1 ">
        <div class="col-span-1 lg:col-span-2 md:col-span-2 sm:col-span-1">
          <Calculator />
        </div>
        <div class="col-span-1">
          <!-- ad placement here  -->
        </div>
      </div>
      <div class="grid grid-cols-1 lg:grid-cols-3 md:grid-cols-3 sm:grid-cols-1">
        <div class="col-span-1 lg:col-span-2 md:col-span-2 sm:col-span-1">
          <Content />
        </div>
        <div class="col-span-1">
          <RelatedLinks />
        </div>
      </div>
      <div class="grid grid-cols-1 lg:grid-cols-3 md:grid-cols-3 sm:grid-cols-1 ">
        <div class="col-span-1 lg:col-span-2 md:col-span-2 sm:col-span-1 ">
          <Famous />
        </div>
        <div class="col-span-1">
          <!-- ad placement here  -->
        </div>
      </div>
      <div class="grid grid-cols-1 lg:grid-cols-3 md:grid-cols-3 sm:grid-cols-1 ">
        <div class="col-span-1 lg:col-span-2 md:col-span-2 sm:col-span-1 ">
          <FAQ />
        </div>
        <div class="col-span-1">
          <!-- ad placement here  -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "primeicons/primeicons.css";

export default {
    name: "IndexPage",
};
</script>