<template>
  <div class="board ">
    <div class="rounded-b-lg bg-gray-200 hover:bg-gray-300 mx-2">
      <div class="board-btn">
        <select
          aria-label="select"
          class="
            cursor-pointer
            focus:text-green-600
            text-xl
            focus:outline-none
            bg-transparent
          "
        >
          <option class="text-lg text-gray-800">Key Result Board</option>
          <option class="text-lg text-gray-800">Key Result Board 2</option>
          <option class="text-lg text-gray-800">Key Result Board 3</option>
        </select>
      </div>
    </div>

    <div class="flex space-x-0">
      <div class="flex place-items-center justify-center cursor-pointer border-gray-700">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-9 w-9 mx-6 border-2 border-gray-400 rounded-lg"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M12 4v16m8-8H4"
          />
        </svg>
      </div>

      <div class="board-widget space-x-1 mr-1">
           <h4>Add Widget</h4>
  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 20 20" fill="currentColor">
  <path d="M5 3a2 2 0 00-2 2v2a2 2 0 002 2h2a2 2 0 002-2V5a2 2 0 00-2-2H5zM5 11a2 2 0 00-2 2v2a2 2 0 002 2h2a2 2 0 002-2v-2a2 2 0 00-2-2H5zM11 5a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V5zM14 11a1 1 0 011 1v1h1a1 1 0 110 2h-1v1a1 1 0 11-2 0v-1h-1a1 1 0 110-2h1v-1a1 1 0 011-1z" />
</svg>
      </div>
    </div>
  </div>
</template>