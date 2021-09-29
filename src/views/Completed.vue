<template>
  <div >
    <h1>Here is my completed projects</h1>
  <Project 
  v-for="completed in completed"
  :key="completed.id"
  :completed="completed"
  
  />





  </div>
</template>


<script>
import json from '/json/completed.json'
import Project from '@/components/Project.vue'

export default {
    components:{
      Project
    },
    data(){
      return {
        completed: json
      }
    }
}
</script>

