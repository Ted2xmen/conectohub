<template>
  <tr class="space-y-4">
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
    <div class="flex place-items-center space-x-2">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-4 w-4"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        stroke-width="2"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M15 19l-7-7 7-7"
        />
      </svg>
      <td
        class="
          flex
          place-items-center
          justify-center
          space-y-2 space-x-1
          overflow-x-scroll
          max-w-md
        "
      >
        <div class="pt-2 py-1" v-for="(n, i) in progress" :key="i">
          <BoxComponent :number="n" color="green" />
        </div>
      </td>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-4 w-4"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        stroke-width="2"
      >
        <path stroke-linecap="round" stroke-linejoin="round" d="M9 5l7 7-7 7" />
      </svg>
    </div>



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
    "color",
  ],
  components: {
    BoxComponent,
  },
};
</script>


