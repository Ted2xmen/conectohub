<template>
  <div id="home" class="pb-12">
    <div class="flex justify-center pb-4">
      <img src="https://www.conectohub.com/wp-content/uploads/2021/01/conectohub_icon_bg_orange_logo_white@2x.png" width="75" height="75" alt="">
    </div>
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
