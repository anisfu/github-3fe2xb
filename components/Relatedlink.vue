<template>
  <div class="max-w-4xl text-left lg:mx-4 md:mx-4">
    <h3 class="text-xl leading-7 font-semibold">Table of Contents</h3>
    <div class="mt-4 overflow-hidden shadow sm:rounded-lg">
      <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
        <table class="w-full text-sm text-left text-gray-500">
              <tbody>
                <tr v-for="item in listLinks" :key="item.id" class="bg-white border-b hover:bg-gray-50">
                  <a v-if="item.isLink" :href="item.link" target="_blank" rel="noopener noreferrer">
                    <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap">
                        {{ item.label }}
                    </th>
                  </a>
                  <th v-if="!item.isLink" scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap">
                      {{ item.label }}
                  </th>
                </tr>
              </tbody>
          </table>
      </div>
    </div>
    <div class="flex justify-center pt-4 space-x-2">
      <!-- footer will be here  -->
    </div>
  </div>
</template>

<script>

export default {
  name: "RelatedLinks",
  data() {
    return {
      listLinks: [
              {
                "id": "646a6cf6-c04e-4d19-892e-ddb79d2552d2",
                "label": "Baby Age Calculator",
                "link": "https://baby-age-en.vercel.app/",
                "isLink": true
              },
              {
                "id": "e40c9706-cf25-4ef8-a748-9c741c61280b",
                "label": "Dog Age Calculator",
                "link": "",
                "isLink": false
              },
              {
                "id": "158db849-a143-4bbc-a757-48d7f25802ca",
                "label": "Birthday Calculator",
                "link": "https://birthday-calculator-en.vercel.app/",
                "isLink": true
              },
              {
                "id": "627154a4-b45d-4768-9a9d-aabef64ecb44",
                "label": "Cat Age Calculator",
                "link": "",
                "isLink": false
              },
              {
                "id": "e114e454-ee78-43d9-ab90-14bf3e9fbe80",
                "label": "Day Calculator",
                "link": "",
                "isLink": false
              },
              {
                "id": "2cb27274-7182-4d9c-a96b-70a2a3a76cb1",
                "label": "Future Age Calculator",
                "link": "",
                "isLink": false
              },
              {
                "id": "81764443-f1f6-4c4c-ae0e-d79c4e9d99cd",
                "label": "Zodiac Sign Calculator",
                "link": "",
                "isLink": false
              }
            ]
    }
  }
  // computed: {
  //   getLinks() {
  //     return this.$store.state.links.listLinks;
  //   }
  // },
  // created() {
  //   this.$store.dispatch('links/fetchRelatedLinks');
  // }
}
</script>