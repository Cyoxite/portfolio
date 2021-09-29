<template>
    

<div class="completed" v-bind:key="completed.id" >
<h3> {{completed.name}}<button @click='toggle = !toggle'>Show more</button></h3>
<div class="Show" v-show='!toggle'>
<div class="gallery">
<img class="miniature" v-for="photo in completed.photo"
  :key="photo.id" :src="photo.link">
  
  </div>
<div class="description">{{completed.description}}</div>
<div class="technology">Technology</div>
</div>
</div>

</template>

<script>
export default {
    data () {
   return {
     toggle: true
   }
    },
    props: 
    ['completed']

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.miniature{
    max-height: 9%;
    max-width: 9%;
    padding-inline: 5px;
}
</style>