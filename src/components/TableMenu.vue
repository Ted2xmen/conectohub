<template>
  <div class="flex place-items-center justify-between py-8">
    <div>
      <div class="flex place-items-center">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-28 w-28 text-red-700"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M9 17v-2m3 2v-4m3 4v-6m2 10H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"
          />
        </svg>
        <h1 class="text-5xl font-semibold text-gray-700">Key Result Board</h1>
      </div>
    </div>

    <div class="flex space-x-6">
      <div class="flex mx-2 cursor-pointer">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6 mx-2 text-gray-600"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
          />
        </svg>

        <select
          aria-label="select"
          type="date"
          class="
            focus:text-green-600
            text-lg
            text-gray-700
            focus:outline-none
            bg-transparent
            ml-1
          "
        >
          <option class="text-md text-gray-800 cursor-pointer">All Time</option>
          <option class="text-md text-gray-800">This Week</option>
          <option class="text-md text-gray-800">Last Week</option>
        </select>
      </div>

      <div class="flex mx-2 cursor-pointer">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6 mx-2 text-gray-600"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3 4a1 1 0 011-1h16a1 1 0 011 1v2.586a1 1 0 01-.293.707l-6.414 6.414a1 1 0 00-.293.707V17l-4 4v-6.586a1 1 0 00-.293-.707L3.293 7.293A1 1 0 013 6.586V4z"
          />
        </svg>
        <select
          aria-label="select"
          type="date"
          class="
            focus:text-green-600
            text-lg
            text-gray-700
            focus:outline-none
            bg-transparent
            ml-1
          "
        >
          <option class="text-md text-gray-800 cursor-pointer">Start</option>
          <option class="text-md text-gray-800">Target</option>
          <option class="text-md text-gray-800">Current</option>
        </select>
      </div>

      <div class="flex cursor-pointer">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M12 5v.01M12 12v.01M12 19v.01M12 6a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2z"
          />
        </svg>
      </div>
    </div>
  </div>
</template>