<template>
  <tr class="bg-white">
    <td class="td-text">
      {{ result }}
    </td>

     <!-- <td class="td-text">
      {{ icon }}
    </td> -->
<td > 
    <img v-if="icon" :src="icon" width="25" height="25" alt="icon"> </td>

    <td class="td-text">
      {{ start }}
    </td>

    <td class="td-text">
      <span>{{ target }}</span>
    </td>

    <td class="td-text">
      {{ current }}
    </td>

    <td class="td-text">{{ progress }}</td>

    <td class="td-text">{{ owners }}</td>

    <td class="td-text">{{ last }}</td>
  </tr>
</template>


<script>
export default {
  props: ["result", "icon", "start", "target", "current", "progress", "owners", "last"],
};
</script>