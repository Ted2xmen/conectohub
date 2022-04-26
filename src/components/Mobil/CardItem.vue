<template>
  <div class="p-2 grid grid-cols-1 sm:grid-cols-1 gap-2">
     
    <div class="p-4 rounded-md shadow-md bg-gray-200">
      <div class="flex space-x-2 align-items-center">
        <h2 class="text-lg font-semibold text-gray-600">{{ result }}</h2>
      </div>
       <div class="flex
          max-w-md
          place-items-center
          justify-center
          space-y-2 space-x-1
          overflow-x-scroll">
        <div class="flex py-2">
          <div v-for="progress in progress" :key="progress" class="p-1 gap-2">
            <div class="w-8 h-7 bg-green-700 flex justify-center place-items-center text-white p-2 rounded-md">{{progress}}</div>
          </div>
        </div>
      </div>
      <div class="flex items-center mt-6 space-x-8 text-xs">
        <div class="sm:inline-flex sm:items-center sm:shrink-0">
          <div class="sm:ml-3 mt-1.5 sm:mt-0">
            <div class="text-gray-500 font-semibold">Start</div>

            <div class="font-medium text-lg">{{ start }}</div>
          </div>
        </div>

        <div class="sm:inline-flex sm:items-center sm:shrink-0">
          <div class="sm:ml-3 mt-1.5 sm:mt-0">
            <div class="text-gray-500 font-semibold">Target</div>

            <div class="font-medium text-lg">{{ target }}</div>
          </div>
        </div>

        <div class="sm:inline-flex sm:items-center sm:shrink-0">
          <div class="sm:ml-3 mt-1.5 sm:mt-0">
            <dt class="text-gray-500 font-semibold">Current</dt>

            <dd class="font-medium text-lg">{{ current }}</dd>
          </div>
        </div>

        <div class="flex items-center p-2 space-x-2 justify-end overflow-hidden">
          <div><svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-600" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
  <path stroke-linecap="round" stroke-linejoin="round" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
</svg></div>

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
            <div class="text-gray-500 font-semibold">Last Checkin</div>

            <div class="font-medium text-lg">{{ last }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {
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