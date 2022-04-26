<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 gap-2">

<div class="bg-yellow-200 p-4 my-2 mx-2 rounded-md">


        <div class="grid items-center space-x-2 text-sm">
      <div>
        <a href="#" class="text-blue-500 font-bold hover:underline">
            {{result}}</a>
      </div>

      <div class="text-gray-500">Start: {{ start }}</div>

      <div>
        <span> Target: {{ target }}</span>
      </div>
    </div>

    <div class="text-sm text-gray-700">Current {{ current }}</div>

    <div id="owners" class="flex items-center -space-x-2 justify-start overflow-hidden">
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

         <div class="flex
          space-y-2 space-x-1
          overflow-x-scroll" v-for="(n, i) in progress" :key="i">
          <BoxComponent :number="n" color="green" />
        </div>
</div>



  </div>
</template>


<script>
import BoxComponent from "@/components/Box/BoxComponent.vue";
export default {
    components: {
        BoxComponent
    },
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
};
</script>