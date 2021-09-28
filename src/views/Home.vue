<template>
  <div class="home">
    <img alt="My avatar" src="../assets/Avatar.png" width="120" height="120">
    <HelloWorld msg="Welcome to My Portfolio"/>
    
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
