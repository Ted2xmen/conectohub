<template>
  <div class="flex flex-wrap">
    <div class="w-full text-center">
      <button
        ref="btnRef"
        v-on:mouseenter="toggleTooltip()"
        v-on:mouseleave="toggleTooltip()"
        class="
          active:bg-gray-600
          font-bold
          text-sm
          ease-linear
          transition-all
          duration-1000"
        type="button"
      >
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
      </button>

      <div
        ref="tooltipRef"
        v-bind:class="{ hidden: !tooltipShow, block: tooltipShow }"
        class="
          bg-gray-200
          w-56
          opacity-100
          text-gray-200
          h-56
          shadow-md
          z-50
          max-w-md
          rounded-lg
      "
      >
  
        <div class="tooltip flex justify-center mx-auto items-center align-items-end">
      
          <a href="#">
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
                d="M8 12h.01M12 12h.01M16 12h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
              /></svg
          ></a>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import { createPopper } from "@popperjs/core";

export default {
  props: ["number", "color"],
  components: {},
  data() {
    return {
      tooltipShow: false,
    };
  },
  methods: {
    toggleTooltip: function () {
      if (this.tooltipShow) {
        this.tooltipShow = false;
      } else {
        this.tooltipShow = true;
        createPopper(this.$refs.btnRef, this.$refs.tooltipRef, {
          placement: "top",
        });
      }
    },
  },
};
</script>