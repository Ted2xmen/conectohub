<template>
  <div class="board">
  <div class="flex place-items-center justify-center cursor-pointer border-gray-700">
    
          <div class="rounded-lg bg-gray-200 hover:bg-gray-300 mx-2">
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
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-7 w-7 mx-6  md:border-2  md:border-gray-300 rounded-lg"
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

    <div class="flex mr-12 md:mr-4">
      <div class="board-home">
<svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
  <path stroke-linecap="round" stroke-linejoin="round" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
</svg>


      </div>
      <div class="board-widget space-x-0 ">
           <h4>Add Widget</h4>
  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 20 20" fill="currentColor">
  <path d="M5 3a2 2 0 00-2 2v2a2 2 0 002 2h2a2 2 0 002-2V5a2 2 0 00-2-2H5zM5 11a2 2 0 00-2 2v2a2 2 0 002 2h2a2 2 0 002-2v-2a2 2 0 00-2-2H5zM11 5a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V5zM14 11a1 1 0 011 1v1h1a1 1 0 110 2h-1v1a1 1 0 11-2 0v-1h-1a1 1 0 110-2h1v-1a1 1 0 011-1z" />
</svg>
      </div>
    </div>
  </div>
</template>