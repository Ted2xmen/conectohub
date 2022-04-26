<template>
  <tr class="divide-y">
    <td class="td-text divide-y">
      {{ result }}
    </td>

    <td class="td-text">
      <img v-if="icon" :src="icon" width="25" height="25" alt="icon" />
    </td>

    <td class="td-text">
      {{ start }}
    </td>

    <td class="td-text">
      <span>{{ target }}</span>
    </td>

    <td class="">
      <span
        class="
          text-sm
          p-1.5
          rounded
          text-gray-600
          hover:text-gray-100
          bg-yellow-500
        "
        >{{ current }}</span
      >
    </td>

    <!-- {{ progress }}  -->
      <td class="flex justify-center space-x-1 bg-red-300" >
        ⬅️ <div class="overflow-scroll-auto   min-w-24"  v-for="(n,i) in 8" :key="i">
            <BoxComponent number="50" />
         </div> ➡️

    </td>
 

    <td class="td-text">{{ owners }}</td>

    <td class="td-text">{{ last }}</td>
  </tr>
</template>


<script>
import BoxComponent from "@/components/Box/BoxComponent.vue";

export default {
  props: [
    "result",
    "icon",
    "start",
    "target",
    "current",
    "progress",
    "owners",
    "last",
  ],
  components: {
    BoxComponent,
  },
};
</script>


