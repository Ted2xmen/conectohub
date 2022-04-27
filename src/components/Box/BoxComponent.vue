<template>
  <span
    :class="`px-4
      py-0
      flex
      place-items-center
      justify-center
      items-center
      mx-1
      leading-loose
      rounded-md
      w-7
      h-7
      bg-${color}-600
      text-gray-100 
      cursor-pointer
      text-sm
      `"
  >
    {{ number }}
  </span>
</template>


<script>
export default {
  props: ["number", "color"],
};
</script>