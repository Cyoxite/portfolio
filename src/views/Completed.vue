<template>
  <div >
    <h1>Here is my completed projects</h1>
  <Project 
  v-for="completed in completed "
  :key="completed.id"
  :completed="completed"
  
  />





  </div>
</template>


<script>
// import json from '/json/completed.json'
import Project from '@/components/Project.vue'

export default {
    components:{
      Project
    },
    data(){
      return {
        completed: [
          {id:0, name: "project 1", gallery: "gallery", description: "Description 1"},
          {id:1, name: "project 2", gallery: "gallery", description: "Description 2"},
          {id:2, name: "project 3", gallery: "gallery", description: "Description 3"}
        ]
      }
    }
}
</script>

