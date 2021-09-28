<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Hello ! I'm Daniel Polanski from Poland. I Was born in 1995 and code is my passion.
      
    </p>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
