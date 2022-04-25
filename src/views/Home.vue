<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
      <h1 class="text-5xl underline text-red-600"> Conectohub</h1>

  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
