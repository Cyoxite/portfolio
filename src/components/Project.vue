<template>
    

<div class="completed" v-bind:key="completed.id" >
<p>Project name {{completed.name}}</p>
<div class="gallery">Gallery{{completed.gallery}}</div>
<div class="description">Description{{completed.description}}</div>
<div class="technology">Technology</div>

</div>

</template>

<script>
export default {
    props: 
    ['completed']

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>