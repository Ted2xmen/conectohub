<template>
  <div class="container mx-auto justify-center">
    <div>
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


<div class="md:hidden">  
     <TableMenu />
<div v-for="(c, i) in Data" :key="i" >
 
      <CardItem
        :result="c.key"
        :start="c.start"
        :target="c.target"
        :current="c.current"
        :owners="c.owners"
        :last="c.lastcheckin"
        :progress="c.checkinprogress"

      />
    </div>
</div>
    
  </div>
</template>


<script>
import TableMenu from "@/components/TableMenu";
import BoardMenu from "@/components/BoardMenu";

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
    CardItem,
  },
  data() {
    return {
      Data,
    };
  },
};
</script>