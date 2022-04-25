<template>
  <div class="h-screen md:container md:mx-auto justify-center">
    <div class="overflow-auto rounded-lg shadow hidden md:block">
      <table class="w-full">
        <TheadComponent />

        <tbody class="divide-y divide-gray-100" v-for="(c, i) in Data" :key="i">
          <TRComponent
            :result="c.key"
            :icon="c.icon"
            :start="c.start"
            :target="c.target"
            :current="c.current"
            :progress="c.checkinprogress"
            :owners="c.owners"
            :last="c.lastcheckin"
          />
        </tbody>
      </table>
    </div>

    <!-- mobile - card -->

    <!-- <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 md:hidden">
      <div class="bg-white space-y-3 p-4 rounded-lg shadow">
        <div class="flex items-center space-x-2 text-sm">
          <div>
            <a href="#" class="text-blue-500 font-bold hover:underline"
              >#1000</a
            >
          </div>

          <div class="text-gray-500">10/10/2021</div>

          <div>
            <span>Delivered</span
            >
          </div>
        </div>

        <div class="text-sm text-gray-700">
          Kring New Fit office chair, mesh + PU, black
        </div>

        <div class="text-sm font-medium text-black">$200.00</div>
      </div>

      <div class="bg-white space-y-3 p-4 rounded-lg shadow">
        <div class="flex items-center space-x-2 text-sm">
          <div>
            <a href="#" class="text-blue-500 font-bold hover:underline"
              >#1001</a
            >
          </div>

          <div class="text-gray-500">10/10/2021</div>

          <div>
            <span>Shipped</span
            >
          </div>
        </div>

        <div class="text-sm text-gray-700">
          Kring New Fit office chair, mesh + PU, black
        </div>

        <div class="text-sm font-medium text-black">$200.00</div>
      </div>

      <div class="bg-white space-y-3 p-4 rounded-lg shadow">
        <div class="flex items-center space-x-2 text-sm">
          <div>
            <a href="#" class="text-blue-500 font-bold hover:underline"
              >#1002</a
            >
          </div>

          <div class="text-gray-500">10/10/2021</div>

          <div>
            <span>Canceled</span
            >
          </div>
        </div>

        <div class="text-sm text-gray-700">
          Kring New Fit office chair, mesh + PU, black
        </div>

        <div class="text-sm font-medium text-black">$200.00</div>
      </div>
    </div> -->
  </div>
</template>


<script>
import TRComponent from "@/components/Table/TRComponent.vue";
import TheadComponent from "@/components/Table/TheadComponent.vue";

import Data from "../assets/data.json"

export default {
  name: "TableContainer",
  components: {
    TheadComponent,
    TRComponent,
  },
  data() {
    return {
      Data
    }
  }
};
</script>