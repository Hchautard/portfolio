<template>
  <div id="app">
    <!-- <fulfilling-square-spinner
    :animation-duration="4000"
    :size="50"
    :color="'#2c3e50'"
  /> -->
  <HeaderPort />
  <AboutMe />
  <MySkills />
  <MyProjects />
  <ContactMe />
  </div>
</template>

<script>
import HeaderPort from './components/Header.vue'
import AboutMe from './components/Me.vue'
import ContactMe from './components/Contact.vue'
import MyProjects from './components/ProjectRow.vue'
import MySkills from './components/Skill.vue'
// import { FulfillingSquareSpinner } from 'epic-spinners'

export default {
  name: 'App',
  components: {
    HeaderPort,
    AboutMe,
    ContactMe,
    MyProjects,
    MySkills
    // FulfillingSquareSpinner
  }
}

// While the window is loading, the spinner will be displayed. Once the window is loaded, the spinner will disappear and the content will be displayed.
// window.onload = function() {
//   document.getElementById('app').style.display = 'block';
//   document.getElementById('fulfilling-square-spinner').style.display = 'none';
// } 

</script>

<style>
#app {
  font-family:  'Courier New', monospace, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
}
</style>
