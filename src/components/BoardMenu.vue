<template>
  <div class="flex place-items-center py-4 mb-1 px-4 text-gray-600">
    <div class="">
      <div
        class="
          flex
          place-items-center
          cursor-pointer
          border-gray-400
          p-6
          border-b-2
        "
      >
        <select
          aria-label="select"
          class="
            focus:text-green-600
            text-2xl
            focus:outline-none
            bg-transparent
            ml-1
          "
        >
          <option class="text-lg text-gray-800">Key Result Board</option>
          <option class="text-lg text-gray-800">Key Result Board 2</option>
          <option class="text-lg text-gray-800">Key Result Board 3</option>
        </select>
      </div>
    </div>

    <div class="flex space-x-6">
      <div class="flex mx-12 place-items-center cursor-pointer">
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
            d="M12 4v16m8-8H4"
          />
        </svg>
      </div>

      <div
        class="
          flex
          p-8
          text-gray-600
          bg-yellow-300
          border-2 border-yellow-300
          cursor-pointer
        "
      >
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