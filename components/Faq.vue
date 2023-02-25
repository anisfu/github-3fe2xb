<template>
  <div class="max-w-4xl mx-auto text-left">
    <h3 class="text-xl leading-7 font-semibold">FAQs</h3>
    <div class="mt-4 overflow-hidden shadow sm:rounded-lg p-6 bg-[#d9ebd8]">
      <ol class="max-w-md space-y-1 text-gray-500 list-decimal list-inside">
        <li v-for="item in listFAQ" :key="item.id">
            <a class="text-blue-600 underline hover:text-blue-500" :href="item.url" target="_blank" rel="noopener noreferrer"><span class="font-semibold">{{ item.question }}</span></a>
        </li>
      </ol>
    </div>
    <div class="flex justify-center pt-4 space-x-2">
      <!-- footer will be here  -->
    </div>
  </div>
</template>

<script>
export default {
  name: "FAQ",
  data() {
    return {
      listFAQ: [
            {
              "id": "c504d477-dda6-4939-bf72-3c1fddf43ff9",
              "question": "How to calculate age?",
              "url": "how-to-calculate-age"
            },
            {
              "id": "f83321c2-3bcf-4458-bb00-3e2cdbbf502d",
              "question": "How old am I in days?",
              "url": "how-old-am-i-in-days"
            },
            {
              "id": "ddd25d49-a1f6-42a0-994c-f37297ff78bd",
              "question": "How old will we be in 2030?",
              "url": "how-old-will-we-be-in-2030"
            },
            {
              "id": "be3d1d86-49bf-4032-9d83-51daddd8204e",
              "question": "How old will we be in 2050?",
              "url": "how-old-will-we-be-in-2050"
            },
            {
              "id": "2640c548-3490-425d-be26-6b5da73df48c",
              "question": "How many years do people live?",
              "url": "how-many-years-do-people-live"
            },
            {
              "id": "1ccc7cc5-f0db-4f3e-8ac8-3639ecc6ee4b",
              "question": "How to calculate age in years and months?",
              "url": "how-to-calculate-age-in-years-and-months"
            }
          ]
    }
  }
  // computed: {
  //   getFaq() {
  //     return this.$store.state.faq.listFaq;
  //   }
  // },
  // created() {
  //   this.$store.dispatch('faq/fetchFaq');
  // }
};
</script>