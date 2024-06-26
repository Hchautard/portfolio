<template>
  <div id="app">
    <div id="inner-border">
      <!-- <img src="../public/assets/images/nuit_etoilee_wallpaper.jpg" id="wallpaper-painting"> -->
      <HomeScreen />
      <AboutMe />
      <MySkills />
      <MyProjects />
    </div>
  </div>
</template>

<script>
import HomeScreen from './components/HomeScreen.vue'
import AboutMe from './components/Me.vue'
import MyProjects from './components/ProjectRow.vue'
import MySkills from './components/Skill.vue'

export default {
  name: 'App',
  components: {
    HomeScreen,
    AboutMe,
    MyProjects,
    MySkills
  },
}

</script>

<style lang="scss">
  @import "../public/assets/css/const";

  #app {
    font-family:  'Courier New', monospace, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    // background-image: url('../public/assets/images/background_yellow.jpg');
  }

  #wallpaper-painting {
    position: absolute;
    width: 100%;
    height: 100%;
    z-index: -1;
    opacity: 0.6;
    transform: scale(1.1);
    animation: backgroundTransition 5s ease-in-out infinite;
  }

  @keyframes backgroundTransition {
    0% {
      background-image: url('../public/assets/images/nuit_etoilee_wallpaper.jpg');
    }
    100% {
      background-image: none;
    }
  }

  body {
    
    background-color: rgb(0, 0, 100);
  } 


</style>
