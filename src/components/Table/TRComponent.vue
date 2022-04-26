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
        class="rounded bg-yellow-500 p-1.5 text-sm text-gray-600 hover:text-gray-100"
        >{{ current }}</span
      >
    </td>

    <!-- {{ progress }}  -->
    <div class="flex place-items-center justify-start space-x-1">
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
        class="flex max-w-md place-items-center justify-center space-y-2 space-x-1 overflow-x-scroll"
      >
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

    <!-- <td >
      <div class=" space-x-1">
 <div class="flex overflow-hidden">
      <img :src="owners[0].avatar" width="30" class="avatar" alt="">
            <img :src="owners[1].avatar" width="30" class="avatar" alt="">
      <img :src="owners[2].avatar" width="30" class="" alt="avatar">

  </div>

      </div>
     
    </td> -->

    <td>
      <div class="flex items-center -space-x-2 justify-start overflow-hidden">


      
          
        
          


                <div>
       <img
          className="avatar"
          v-if="owners[0].avatar"
          :src="owners[0].avatar"
          alt=""
        />
        <span v-else class="avatar-text">{{owners[0].title.slice(0,1)}}</span>
                </div>

                            <div>
       <img
          className="avatar"
          v-if="owners[1].avatar"
          :src="owners[1].avatar"
          alt=""
        />
        <span v-else class="avatar-text">{{owners[1].title.slice(0,1)}}</span>
                </div>

                            <div>
       <img
          className="avatar"
          v-if="owners[2].avatar"
          :src="owners[2].avatar"
          alt=""
        />
        <span v-else class="avatar-text">{{owners[2].title.slice(0,1)}}</span>
                </div>

        <div>
      
        <span v-if="owners.length > 3" class="avatar-text">2 +</span>
                </div>

                

                

                


    

           





   

        <!-- <div v-if="owners[2]"
          class="-mx-2 flex h-10 w-10 items-center justify-center overflow-hidden rounded-full border-2 border-white"
        >
          <img  :src="owners[2].avatar" />
        </div> -->

        <!-- <div
          class="-mx-2 flex h-10 w-10 items-center justify-center overflow-hidden rounded-full border-2 border-white"
        >
          <img :src="owners[2].avatar" />
        </div> -->

        <!-- <div v-if="owners.length > 2" class="flex items-center justify-center w-10 h-10 -mx-2 overflow-hidden rounded-full border-2 border-white">
        <span class="bg-gray-600 text-white ronuded-full w-10 h-10 flex items-center justify-center">2+</span>
      </div> -->
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
