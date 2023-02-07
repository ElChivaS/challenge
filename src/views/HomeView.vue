<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App" class="mt-5"/>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
