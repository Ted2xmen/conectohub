<template>
  <div class="rounded-lg shadow-md md:container md:mx-auto justify-center">
    <div class="py-4 my-12 rounded-lg bg-gray-200 shadow-md">
      <BoardMenu />
    </div>
    <div class="overflow-auto hidden md:block">
      <TableMenu />
      <table class="w-full">
        <TheadComponent />
        <tbody v-for="(c, i) in Data" :key="i">
          <TRComponent
            :result="c.key"
            :icon="c.icon"
            :start="c.start"
            :target="c.target"
            :current="c.current"
            :progress="c.checkinprogress"
            :owners="c.owners"
            :last="c.lastcheckin"
            :color="c.color"
          />
        </tbody>
      </table>
    </div>

    <!-- mobile - card -->
    <!-- <div v-for="(c, i) in Data" :key="i" class="md:hidden">    
       <Card
            :result="c.key"
            :icon="c.icon"
            :start="c.start"
            :target="c.target"
            :current="c.current"
            :progress="c.checkinprogress"
            :owners="c.owners"
            :last="c.lastcheckin"
            :color="c.color"
     />
      </div> -->

    <div v-for="(c, i) in Data" :key="i" class="md:hidden">
      <CardItem
        :result="c.key"
        :start="c.start"
        :target="c.target"
        :current="c.current"
        :owners="c.owners"
        :last="c.lastcheckin"
      />
    </div>
  </div>
</template>


<script>
import TableMenu from "@/components/TableMenu";
import BoardMenu from "@/components/BoardMenu";

// import Card from '@/components/Mobil/Card.vue'
import CardItem from "@/components/Mobil/CardItem.vue";

import TRComponent from "@/components/Table/TRComponent.vue";
import TheadComponent from "@/components/Table/TheadComponent.vue";

import Data from "../assets/data.json";

export default {
  name: "TableContainer",
  components: {
    TheadComponent,
    TRComponent,
    TableMenu,
    BoardMenu,
    // Card,
    CardItem,
  },
  data() {
    return {
      Data,
    };
  },
};
</script>