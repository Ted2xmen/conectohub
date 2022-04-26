<template>
  <div class="p-2">

    <div class="p-4 rounded-md shadow-md bg-gray-400">
      <div>
        <span class="text-sm">Check-in Progress</span>
        <div class="flex py-2">
          <div v-for="item in 18" :key="item" class="px-1 gap-2">
            <div class="w-6 h-6 bg-green-600 text-white p-1 rounded-md">50</div>
          </div>
        </div>
      </div>

      <div class="flex py-2 space-x-2">
        <h2 class="font-bold" >Key Result</h2>
        <h2 class="text-md text-gray-500">{{ result }}</h2>
      </div>

      <div class="flex items-center mt-6 space-x-8 text-xs">


        <div class="sm:inline-flex sm:items-center sm:shrink-0">
          <div class="sm:ml-3 mt-1.5 sm:mt-0">
            <div class="text-gray-500">Start</div>

            <div class="font-medium">{{ start }}</div>
          </div>
        </div>

        <div class="sm:inline-flex sm:items-center sm:shrink-0">
          <div class="sm:ml-3 mt-1.5 sm:mt-0">
            <div class="text-gray-500">Target</div>

            <div class="font-medium">{{ target }}</div>
          </div>
        </div>

        <div class="sm:inline-flex sm:items-center sm:shrink-0">
          <div class="sm:ml-3 mt-1.5 sm:mt-0">
            <dt class="text-gray-500">Current</dt>

            <dd class="font-medium">{{ current }}</dd>
          </div>
        </div>

        <div class="flex items-center space-x-2 justify-end overflow-hidden">
          <div class="text-gray-500">Owners</div>

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
            <img
              className="avatar"
              v-if="owners[3].avatar"
              :src="owners[3].avatar"
              alt=""
            />
            <span v-else class="avatar-text">{{
              owners[3].title.slice(0, 1)
            }}</span>
          </div>

          <div>
            <span v-if="owners.length > 5" class="avatar-text">2 +</span>
          </div>
        </div>


             <div class="sm:inline-flex sm:items-center sm:shrink-0">
          <div class="sm:ml-3 mt-1.5 sm:mt-0">
            <dt class="text-gray-500">Last Checkin</dt>

            <dd class="font-medium">{{ last }}</dd>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
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
};
</script>