<template lang="">
<div class="projects-card">
  <div v-for="(item, index) in projectData.ProjectsArray" :key="index" class="project-card">
    <img :src="projectData.ProjectsArray[index].link1" alt="">
    <h2>{{projectData.ProjectsArray[index].nom}}</h2>
    <p>{{projectData.ProjectsArray[index].subject}}</p>
  </div>
</div>
</template>
<script>
import jsonProjects from "/project.json";
export default {
  data(){
    return{
      projectData: jsonProjects
    }
  }
}
</script>
<style scoped>
  .projects-card{
    display:flex;
    margin: auto;
  }
  .project-card{
    margin: 20px;
    width: 400px;
    height: 400px;
    background-color: grey;
  }

  img {
    width: 100%;
    height: 150px;
  }
</style>
