<template>
  <div class="max-w-4xl mx-auto text-left">
    <h3 class="text-xl leading-7 font-semibold">Famous Birthday</h3>
    <div class="mt-4 overflow-hidden shadow sm:rounded-lg p-6 bg-[#d9ebd8]">
      <div class="grid grid-cols-2 lg:grid-cols-4 md:grid-cols-4 sm:grid-cols-3 gap-2">
        <div v-for="item in listFamous" :key="item.id" class="w-full max-w-sm bg-white border border-gray-200 rounded-lg shadow">
          <a :href="item.url">
            <div class="flex flex-col items-center py-6">
                <h5 class="m-2 text-xl font-medium text-gray-900 text-center">{{ item.name }}</h5>
                <span class="text-sm text-gray-500">{{ item.title }}</span>
            </div>
          </a>
        </div>

      </div>

    </div>
    <div class="flex justify-center pt-4 space-x-2">
      <!-- footer will be here  -->
    </div>
  </div>
</template>

<script>
export default {
  name: "Famous",
  data() {
    return {
      listFamous: [
            {
              "id": "4a7b5acd-d9c4-4aff-96c5-2c840354adba",
              "name": "Hillary Clinton",
              "title": "President of United State",
              "url": "hillary-clinton"
            },
            {
              "id": "dc4dc007-41f2-4738-b9ec-32d4ea5a3a40",
              "name": "Donald Trump",
              "title": "President of United State",
              "url": "donald-trump"
            },
            {
              "id": "5bce6a58-1ff7-4b61-87d4-4263fe0cc4ec",
              "name": "Jokowi",
              "title": "President of Indonesia",
              "url": "jokowi"
            },
            {
              "id": "322dadd8-4393-4997-a899-dc0ee7186093",
              "name": "Salman bin Abdulaziz Al Saud",
              "title": "King of Saudi Arabia",
              "url": "salman-bin-abdulaziz-al-saud"

            },
            {
              "id": "1f37d6e0-4ef3-4afe-8459-4a72446cffb9",
              "name": "Sheikh Tamim bin Hamad Al Thani",
              "title": "President of Qatar",
              "url": "sheikh-tamim-bin-hamad-al-thani"
            }
          ]
    }
  }
  // computed: {
  //   getFamous() {
  //     return this.$store.state.famous.listFamous;
  //   }
  // },
  // created() {
  //   this.$store.dispatch('famous/fetchFamous');
  // }
};
</script>