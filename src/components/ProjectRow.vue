<template>
    <div id="my-projects">
      <img src="../../public/assets/images/monet_2.jpg" id="wallpaper-painting-3">
        <!-- <div id="my-projects-title">
            <h1>Mes projets</h1>
        </div> -->
        <div id="my-projects-body">
          <div v-for="project in projects"
            v-bind:key="project.id"
            class="my-projects-card">
            <ProjectCard 
              :projects="project"
            />
          </div>
        </div>
    </div>
</template>
<script>
  import ProjectsJSON from '../data/projects.json'
  import ProjectCard from './ProjectCard.vue'

  export default {
    name: 'ProjectRow',
    components: {
      ProjectCard
    },
    data() {
      return {
        projects : ProjectsJSON.projects,
      }
    }

  }
</script>
  
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
      @import "../../public/assets/css/const.scss";

      h1 {
        margin-top: 100px;
        display: flex;
        justify-content: center;
      }

      #my-projects {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        // background-image: url('../../public/assets/images/monet_2.jpg');
        height: 100vh;
      }

      #wallpaper-painting-3 {
          position: absolute;
          width: 209vh; 
          height: 108%;
          z-index: -1;
          // opacity: ;
        }

      #my-projects-body {
        height: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        margin: 50px;
      }

      .my-projects-card {
        width: 400px;
        height: 275px; 
        display: flex;
        flex-direction: column;
        overflow-wrap: break-word;
        margin: 40px;
        box-shadow: rgba(0, 0, 0, 0.25) 0px 14px 28px, rgba(0, 0, 0, 0.22) 0px 10px 10px;
      }
</style>
  