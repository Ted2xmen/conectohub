<template>
  <span
    :class="`px-2
      py-0
      mx-1
      leading-loose
      rounded-md
      w-8
      h-8
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