<template>
    <div class="max-w-4xl mx-auto text-center">
      <h2 class="text-2xl leading-7 font-semibold">Age Calculator Online</h2>
      <form @submit.prevent="onSubmitCalculate" v-if="!isCalculate">
        <div class="mt-8 overflow-hidden shadow sm:rounded-lg p-6 bg-[#d9ebd8]">
            <div>
              <label
                for="borndate"
                class="
                  block
                  mb-2
                  text-sm
                  font-medium
                  text-gray-900

                "
                >Born Date</label
              >
              <div class="grid grid-cols-3 gap-3">
                <select
                  id="bornDay"
                  name="bornDay"
                  v-model="bornDay"
                  class="
                    bg-gray-50
                    border border-gray-300
                    text-gray-900 text-sm
                    rounded-lg
                    focus:ring-blue-500 focus:border-blue-500
                    block
                    w-full
                    p-2.5
                  "
                >
                  <option value="" selected>Day</option>
                  <option value="01">1</option>
                  <option value="02">2</option>
                  <option value="03">3</option>
                  <option value="04">4</option>
                  <option value="05">5</option>
                  <option value="06">6</option>
                  <option value="07">7</option>
                  <option value="08">8</option>
                  <option value="09">9</option>
                  <option value="10">10</option>
                  <option value="11">11</option>
                  <option value="12">12</option>
                  <option value="13">13</option>
                  <option value="14">14</option>
                  <option value="15">15</option>
                  <option value="16">16</option>
                  <option value="17">17</option>
                  <option value="18">18</option>
                  <option value="19">19</option>
                  <option value="20">20</option>
                  <option value="21">21</option>
                  <option value="22">22</option>
                  <option value="23">23</option>
                  <option value="24">24</option>
                  <option value="25">25</option>
                  <option value="26">26</option>
                  <option value="27">27</option>
                  <option value="28">28</option>
                  <option value="29">29</option>
                  <option value="30">30</option>
                  <option value="31">31</option>
                </select>
                <select
                  id="bornMonth"
                  name="bornMonth"
                  v-model="bornMonth"
                  class="
                    bg-gray-50
                    border border-gray-300
                    text-gray-900 text-sm
                    rounded-lg
                    focus:ring-blue-500 focus:border-blue-500
                    block
                    w-full
                    p-2.5



                  "
                >
                  <option value="" selected>Month</option>
                  <option value="01">January</option>
                  <option value="02">February</option>
                  <option value="03">March</option>
                  <option value="04">April</option>
                  <option value="05">Mey</option>
                  <option value="06">June</option>
                  <option value="07">July</option>
                  <option value="08">Agustus</option>
                  <option value="09">September</option>
                  <option value="10">Oktober</option>
                  <option value="11">November</option>
                  <option value="12">Desember</option>
                </select>
                <select
                  id="bornYear"
                  name="bornYear"
                  v-model="bornYear"
                  class="
                    bg-gray-50
                    border border-gray-300
                    text-gray-900 text-sm
                    rounded-lg
                    focus:ring-blue-500 focus:border-blue-500
                    block
                    w-full
                    p-2.5



                  "
                >
                  <option value="" selected>Year</option>
                  <option value="1970">1970</option>
                  <option value="1971">1971</option>
                  <option value="1972">1972</option>
                  <option value="1973">1973</option>
                  <option value="1974">1974</option>
                  <option value="1975">1975</option>
                  <option value="1976">1976</option>
                  <option value="1977">1977</option>
                  <option value="1978">1978</option>
                  <option value="1979">1979</option>
                  <option value="1980">1980</option>
                  <option value="1981">1981</option>
                  <option value="1982">1982</option>
                  <option value="1983">1983</option>
                  <option value="1984">1984</option>
                  <option value="1985">1985</option>
                  <option value="1986">1986</option>
                  <option value="1987">1987</option>
                  <option value="1988">1988</option>
                  <option value="1989">1989</option>
                  <option value="1990">1990</option>
                  <option value="1991">1991</option>
                  <option value="1992">1992</option>
                  <option value="1993">1993</option>
                  <option value="1994">1994</option>
                  <option value="1995">1995</option>
                  <option value="1996">1996</option>
                  <option value="1997">1997</option>
                  <option value="1998">1998</option>
                  <option value="1999">1999</option>
                  <option value="2000">2000</option>
                  <option value="2001">2001</option>
                  <option value="2002">2002</option>
                  <option value="2003">2003</option>
                  <option value="2004">2004</option>
                  <option value="2005">2005</option>
                  <option value="2006">2006</option>
                </select>
              </div>
            </div>
            <div class="mt-3">
              <label
                for="dayToDate"
                class="
                  block
                  mb-2
                  text-sm
                  font-medium
                  text-gray-900

                "
                >Day to Date</label
              >
              <div class="grid grid-cols-3 gap-3">
                <select
                  id="dayDay"
                  name="dayDay"
                  v-model="dayDay"
                  class="
                    bg-gray-50
                    border border-gray-300
                    text-gray-900 text-sm
                    rounded-lg
                    focus:ring-blue-500 focus:border-blue-500
                    block
                    w-full
                    p-2.5



                  "
                >
                  <option value="01" selected>1</option>
                  <option value="02">2</option>
                  <option value="03">3</option>
                  <option value="04">4</option>
                  <option value="05">5</option>
                  <option value="06">6</option>
                  <option value="07">7</option>
                  <option value="08">8</option>
                  <option value="09">9</option>
                  <option value="10">10</option>
                  <option value="11">11</option>
                  <option value="12">12</option>
                  <option value="13">13</option>
                  <option value="14">14</option>
                  <option value="15">15</option>
                  <option value="16">16</option>
                  <option value="17">17</option>
                  <option value="18">18</option>
                  <option value="19">19</option>
                  <option value="20">20</option>
                  <option value="21">21</option>
                  <option value="22">22</option>
                  <option value="23">23</option>
                  <option value="24">24</option>
                  <option value="25">25</option>
                  <option value="26">26</option>
                  <option value="27">27</option>
                  <option value="28">28</option>
                  <option value="29">29</option>
                  <option value="30">30</option>
                  <option value="31">31</option>
                </select>
                <select
                  id="dayMonth"
                  name="dayMonth"
                  v-model="dayMonth"
                  class="
                    bg-gray-50
                    border border-gray-300
                    text-gray-900 text-sm
                    rounded-lg
                    focus:ring-blue-500 focus:border-blue-500
                    block
                    w-full
                    p-2.5



                  "
                >
                  <option value="01" selected>January</option>
                  <option value="02">February</option>
                  <option value="03">March</option>
                  <option value="04">April</option>
                  <option value="05">Mey</option>
                  <option value="06">June</option>
                  <option value="07">July</option>
                  <option value="08">Agustus</option>
                  <option value="09">September</option>
                  <option value="10">Oktober</option>
                  <option value="11">November</option>
                  <option value="12">Desember</option>
                </select>
                <select
                  id="dayYear"
                  name="dayYear"
                  v-model="dayYear"
                  class="
                    bg-gray-50
                    border border-gray-300
                    text-gray-900 text-sm
                    rounded-lg
                    focus:ring-blue-500 focus:border-blue-500
                    block
                    w-full
                    p-2.5



                  "
                >
                  <option value="1970" selected>1970</option>
                  <option value="1971">1971</option>
                  <option value="1972">1972</option>
                  <option value="1973">1973</option>
                  <option value="1974">1974</option>
                  <option value="1975">1975</option>
                  <option value="1976">1976</option>
                  <option value="1977">1977</option>
                  <option value="1978">1978</option>
                  <option value="1979">1979</option>
                  <option value="1980">1980</option>
                  <option value="1981">1981</option>
                  <option value="1982">1982</option>
                  <option value="1983">1983</option>
                  <option value="1984">1984</option>
                  <option value="1985">1985</option>
                  <option value="1986">1986</option>
                  <option value="1987">1987</option>
                  <option value="1988">1988</option>
                  <option value="1989">1989</option>
                  <option value="1990">1990</option>
                  <option value="1991">1991</option>
                  <option value="1992">1992</option>
                  <option value="1993">1993</option>
                  <option value="1994">1994</option>
                  <option value="1995">1995</option>
                  <option value="1996">1996</option>
                  <option value="1997">1997</option>
                  <option value="1998">1998</option>
                  <option value="1999">1999</option>
                  <option value="2000">2000</option>
                  <option value="2001">2001</option>
                  <option value="2002">2002</option>
                  <option value="2003">2003</option>
                  <option value="2004">2004</option>
                  <option value="2005">2005</option>
                  <option value="2006">2006</option>
                  <option value="2007">2007</option>
                  <option value="2008">2008</option>
                  <option value="2009">2009</option>
                  <option value="2010">2010</option>
                  <option value="2011">2011</option>
                  <option value="2012">2012</option>
                  <option value="2013">2013</option>
                  <option value="2014">2014</option>
                  <option value="2015">2015</option>
                  <option value="2016">2016</option>
                  <option value="2017">2017</option>
                  <option value="2018">2018</option>
                  <option value="2019">2019</option>
                  <option value="2020">2020</option>
                  <option value="2021">2021</option>
                  <option value="2022">2022</option>
                  <option value="2023">2023</option>
                  <option value="2024">2024</option>
                  <option value="2025">2025</option>
                  <option value="2026">2026</option>
                  <option value="2027">2027</option>
                  <option value="2028">2028</option>
                  <option value="2029">2029</option>
                  <option value="2030">2030</option>
                </select>
              </div>
            </div>
        </div>
        <div class="overflow-hidden p-6">
          <div class="mt-3">
              <button
                type="submit"
                :disabled="!bornDay && !bornMonth && !bornYear"
                class="
                  text-white
                  bg-[#ffa700]
                  hover:bg-[#4285F4]/90
                  disabled:hover:bg-[#ffa500]
                  focus:ring-4 focus:outline-none focus:ring-[#4285F4]/50
                  font-medium
                  rounded-lg
                  text-sm
                  px-5
                  py-2.5
                  text-center
                  inline-flex
                  items-center
                  mr-2
                  mb-2
                "
              >
                <i class="pi pi-calculator mr-2"></i>
                {{ isLoading ? "Calculating..." : "Calculate" }}
              </button>
              <button
                @click="onClear"
                type="button"
                class="
                  text-white
                  bg-[#d62d20]
                  hover:bg-[#4285F4]/90
                  focus:ring-4 focus:outline-none focus:ring-[#4285F4]/50
                  font-medium
                  rounded-lg
                  text-sm
                  px-5
                  py-2.5
                  text-center
                  inline-flex
                  items-center
                  mr-2
                  mb-2
                "
              >
                <i class="pi pi-refresh mr-2"></i>
                Clear
              </button>
          </div>
        </div>
      </form>
      <div v-if="isCalculate" class="mt-8 overflow-hidden shadow sm:rounded-lg p-6 bg-[#d9ebd8]">
        <div id="result">
          <div class="grid grid-cols-2 gap-3">
            <div>
              <div class="flex">
                <i class="pi pi-calendar mr-2 mt-1"></i>
                <h3 class="text-lg font-semibold">Your Date of Birth is</h3>
              </div>
              <div class="text-left ml-6">
                <p class="text-md">{{ dateOfBirth }}</p>
              </div>
            </div>
            <div class="text-left">
              <div>
                <h3 class="text-lg font-semibold">Days Left in Next Birthday</h3>
              </div>
              <div class="mt-1">
                <div class="w-full bg-gray-300 rounded-full h-6 justify-between flex">
                  <div class="bg-yellow-500 h-6 rounded-full" :style="{ width:  percentageDaysLeft + '%' }">
                  <div class="ml-2">
                      <p class="text-md">
                        {{ daysLeft }}
                      </p>
                  </div>
                  </div>
                  <i class="pi pi-gift mr-2 mt-1"></i>
                </div>
              </div>
            </div>
          </div>
          <div class="grid grid-cols-2 mt-12">
            <div>
              <div class="flex">
                <i class="pi pi-chart-line mr-2 mt-1"></i>
                <h3 class="text-lg font-semibold">Your Age is</h3>
              </div>
              <div class="flex ml-6">
                <p class="text-md font-semibold mr-2 border-r border-gray-400 p-2"><span class="text-yellow-600 text-xl mr-1">{{ ageYears }}</span> Years</p>
                <p class="text-md font-semibold mr-2 border-r border-gray-400 p-2"><span class="text-yellow-600 text-xl mr-1">{{ overMonths }}</span> Months</p>
                <p class="text-md font-semibold mr-2 p-2"><span class="text-yellow-600 text-xl mr-1">{{ overDays }}</span> Days</p>
              </div>
            </div>
            <div>
              <h3 class="text-lg font-semibold text-left mb-2">Your Half Birthday is on</h3>
              <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
                  <table class="w-full text-sm text-left text-gray-500">
                      <tbody>
                          <tr class="border-b border-gray-200">
                              <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap bg-gray-50  ">
                                  In Years
                              </th>
                              <td class="px-6 py-4">
                                  {{ ageYears }} Years
                              </td>
                          </tr>
                          <tr class="border-b border-gray-200 ">
                              <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap bg-gray-50  ">
                                  In Months
                              </th>
                              <td class="px-6 py-4">
                                  {{ ageMonths }} Months
                              </td>
                          </tr>
                          <tr class="border-b border-gray-200 ">
                              <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap bg-gray-50  ">
                                  In Weeks
                              </th>
                              <td class="px-6 py-4">
                                  {{ ageWeeks }} Weeks
                              </td>
                          </tr>
                          <tr class="border-b border-gray-200 ">
                              <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap bg-gray-50  ">
                                  In Days
                              </th>
                              <td class="px-6 py-4">
                                  {{ ageDays }} Days
                              </td>
                          </tr>
                          <tr class="border-b border-gray-200 ">
                              <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap bg-gray-50  ">
                                  In Hours
                              </th>
                              <td class="px-6 py-4">
                                  {{ ageHours }} Hours
                              </td>
                          </tr>
                          <tr class="border-b border-gray-200 ">
                              <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap bg-gray-50  ">
                                  In Minutes
                              </th>
                              <td class="px-6 py-4">
                                  {{ ageMinutes }} Minutes
                              </td>
                          </tr>
                          <tr class="border-b border-gray-200 ">
                              <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap bg-gray-50  ">
                                  In Seconds
                              </th>
                              <td class="px-6 py-4">
                                  {{ ageSeconds }} Seconds
                              </td>
                          </tr>
                      </tbody>
                  </table>
              </div>
            </div>
          </div>
          <div class="grid mt-12 text-left">
            <h3 class="text-lg font-semibold">Amazing Facts about You</h3>
            <h4 class="text-md font-normal">Interesting facts about you</h4>
          </div>
          <div class="grid grid-cols-1 lg:grid-cols-2 md:grid-cols-2 sm:grid-cols-1 x:grid-cols-1">
            <div class="border-b border-r border-gray-400 p-3 justify-center">
              <div class="flex justify-center">
                <i class="pi pi-chart-line mr-2 mt-1"></i>
                <h3 class="text-lg font-normal">Breaths</h3>
              </div>
              <div class="flex justify-center">
                <p class="text-md font-semibold mr-2"><span class="text-yellow-600 text-xl mr-1 ">{{ breaths }}</span> breaths of air</p>
              </div>
            </div>
            <div class="border-b border-gray-400 p-3">
              <div class="flex justify-center">
                <i class="pi pi-chart-line mr-2 mt-1"></i>
                <h3 class="text-lg font-normal">Heart Beats</h3>
              </div>
              <div class="flex justify-center">
                <p class="text-md font-semibold mr-2"><span class="text-yellow-600 text-xl mr-1">{{ beats }}</span> times</p>
              </div>
            </div>
            <div class="border-r border-gray-400 p-3">
              <div class="flex justify-center">
                <i class="pi pi-chart-line mr-2 mt-1"></i>
                <h3 class="text-lg font-normal">Laughing Time</h3>
              </div>
              <div class="flex justify-center">
                <p class="text-md font-semibold mr-2"><span class="text-yellow-600 text-xl mr-1">{{ laughing }}</span> times</p>
              </div>
            </div>
            <div class="p-3">
              <div class="flex justify-center">
                <i class="pi pi-chart-line mr-2 mt-1"></i>
                <h3 class="text-lg font-normal">Sleeping Time</h3>
              </div>
              <div class="flex justify-center">
                <p class="text-md font-semibold mr-2"><span class="text-yellow-600 text-xl mr-1">{{ sleeping }}</span> Years</p>
              </div>
            </div>
          </div>
          <div class="grid justify-center text-center mt-5">
            <button
              @click="onClear"
              type="button"
              class="
                text-white
                bg-[#d62d20]
                hover:bg-[#4285F4]/90
                focus:ring-4 focus:outline-none focus:ring-[#4285F4]/50
                font-medium
                rounded-lg
                text-sm
                px-5
                py-2.5
                text-center
                inline-flex
                items-center

                mr-2
                mb-2
              "
            >
              <i class="pi pi-refresh mr-2"></i>
              Re-Calculate
            </button>
          </div>
        </div>
      </div>
    </div>
</template>

<script>

export default {
  name: "Calculator",
  data() {;
    const today = new Date();
    return {
      ageYears: 0,
      overMonths: 0,
      overDays: 0,
      ageMonths: 0,
      ageWeeks: 0,
      ageDays: 0,
      ageHours: 0,
      ageMinutes: 0,
      ageSeconds: 0,
      daysLeft: 0,
      percentageDaysLeft: 0,
      isCalculate: false,
      isLoading: false,
      bornDay: "",
      bornMonth: "",
      bornYear: "",
      dateOfBirth: "",
      dayDay: String(today.getDate()).padStart(2, "0"),
      dayMonth: String(today.getMonth() + 1).padStart(2, "0"),
      dayYear: today.getFullYear(),
      breaths: 0,
      beats: 0,
      laughing: 0,
      sleeping: 0,
    };
  },
  methods: {
    onClear() {
      this.isCalculate = false;
      this.bornDay = "";
      this.bornMonth = "";
      this.bornYear = "";
      const today = new Date();
      this.dayDay = String(today.getDate()).padStart(2, "0");
      this.dayMonth = String(today.getMonth() + 1).padStart(2, "0");
      this.dayYear = today.getFullYear();
    },
    onSubmitCalculate() {
      if (this.bornDay && this.bornMonth && this.bornYear) {
        this.isLoading = true;
        const bornDate = `${this.bornYear}-${this.bornMonth}-${this.bornDay}`;
        const bornDateParse = new Date(bornDate);
        const enUS = bornDateParse.toLocaleDateString('en-US', { dateStyle: 'full' });
        this.dateOfBirth = enUS;

        let today = new Date();

        const toDayDate = `${this.dayYear}-${this.dayMonth}-${this.dayDay}`;
        const toDayDateParse = new Date(toDayDate);
        const ageInMilliseconds =
          toDayDateParse.getTime() - bornDateParse.getTime();
        const ageInYears = Math.floor(
          ageInMilliseconds / (1000 * 60 * 60 * 24 * 365)
        );
        const ageInMonths = Math.floor(
          ageInMilliseconds / (1000 * 60 * 60 * 24 * 30)
        );
        const ageInWeeks = Math.floor(
          ageInMilliseconds / (1000 * 60 * 60 * 24 * 7)
        );
        const ageInDays = Math.floor(
          ageInMilliseconds / (1000 * 60 * 60 * 24)
        );
        const ageInHours = Math.floor(
          ageInMilliseconds / (1000 * 60 * 60)
        );
        const ageInMinutes = Math.floor(
          ageInMilliseconds / (1000 * 60)
        );
        const ageInSeconds = Math.floor(
          ageInMilliseconds / (1000)
        );

        const diffInMilliseconds = today.valueOf() - bornDateParse.valueOf();
        const yearInMs = 365.25 * 24 * 60 * 60 * 1000;
        const monthInMs = yearInMs / 12;
        const dayInMs = 24 * 60 * 60 * 1000;
        const months = Math.floor((diffInMilliseconds % yearInMs) / monthInMs);
        const days = Math.floor((diffInMilliseconds % monthInMs) / dayInMs);


        const birthday = `${today.getFullYear()}-${this.bornMonth}-${this.bornDay}`;
        const birthdayParse = new Date(birthday);
        if (today.getTime() > birthdayParse.getTime()) {
          birthdayParse.setFullYear(birthdayParse.getFullYear() + 1);
        }
        const diffTime = Math.abs(birthdayParse.valueOf() - today.valueOf());
        const diffDays = Math.ceil(diffTime / (1000 * 60 * 60 * 24));

        let breathsTemp = ageInMinutes * 16;

        let beatsTemp = ageInMinutes * 80;

        let laughingTemp = ageInDays * 15;

        let sleepingTemp = ageInDays * 8;

        this.daysLeft = diffDays;
        this.percentageDaysLeft = Math.floor(diffDays / 365 * 100);
        this.ageYears = ageInYears;
        this.overMonths = months;
        this.overDays = days;
        this.ageMonths = ageInMonths;
        this.ageWeeks = ageInWeeks;
        this.ageDays = ageInDays;
        this.ageHours = ageInHours;
        this.ageMinutes = ageInMinutes;
        this.ageSeconds = ageInSeconds;
        this.isCalculate = true;
        this.isLoading = false;
        this.breaths = breathsTemp;
        this.beats = beatsTemp;
        this.laughing = laughingTemp;
        this.sleeping = sleepingTemp;
      }
    },
  },
};
</script>