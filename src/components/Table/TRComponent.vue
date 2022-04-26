<template>
  <tr class="space-y-4 border-b-2 border-gray-100 hover:bg-gray-100">
    <td class="td-text">
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

    <td>
      <span
        class="
          p-1.5
          text-sm text-gray-600"
        >
        <span class="w-2 h-2 px-2 m-1 bg-yellow-500 rounded-sm"></span>
        {{ current }} </span
      >
    </td>

    <div class="flex place-items-center place-self-center justify-center align-items-center space-x-4">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-4 w-4"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        stroke-width="2">
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M15 19l-7-7 7-7"
        />
      </svg>
      <td
        class="
          flex
          pb-2
          max-w-md
          place-items-center
          justify-center
          space-y-2 space-x-1
          overflow-x-scroll">
        <div class="py-1 pt-2" v-for="(n, i) in progress" :key="i">
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

    <td>
      <div class="flex  overflow-x-auto   max-w-md items-center -space-x-1 justify-center overflow-hidden py-2">
        <div>
          <img
            className="avatar"
            v-if="owners[0].avatar"
            :src="owners[0].avatar"
            alt=""
          />
          <span v-else class="avatar-text">{{
            owners[0].title.slice(0, 1)
          }}</span>
        </div>

        <div>
          <img
            className="avatar"
            v-if="owners[1].avatar"
            :src="owners[1].avatar"
            alt=""
          />
          <span v-else class="avatar-text">{{
            owners[1].title.slice(0, 1)
          }}</span>
        </div>

        <div>
          <img
            className="avatar"
            v-if="owners[2].avatar"
            :src="owners[2].avatar"
            alt=""
          />
          <span v-else class="avatar-text">{{
            owners[2].title.slice(0, 1)
          }}</span>
        </div>

        <div>
          <span v-if="owners.length > 3" class="avatar-text">2 +</span>
        </div>
      </div>
    </td>

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
