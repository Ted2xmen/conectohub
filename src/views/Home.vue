<template>
  <div id="home" class="pb-24">
   
    <TableContainer />

  </div>
</template>

<script>
// @ is an alias to /src
import TableContainer from '@/components/TableContainer.vue'

export default {
  name: 'Home',
  components: {
    TableContainer
  }
}
</script>
