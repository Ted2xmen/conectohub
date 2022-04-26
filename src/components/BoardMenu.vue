<template>
  <div class="board">
    <div class="rounded-t-lg bg-gray-200 hover:bg-gray-300 mx-2">
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

    <div class="flex space-x-10">
      <div class="flex place-items-center cursor-pointer">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-8 w-8 mx-8"
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

      <div class="board-widget">
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
            d="M12 6v6m0 0v6m0-6h6m-6 0H6"
          />
        </svg>
        <h4>Add Widget</h4>
      </div>
    </div>
  </div>
</template>