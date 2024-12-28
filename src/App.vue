<template>
  <div id="app">
    <div id="container-app" class="neomorphic">
      <MeBlock />
      <ExperienceBlock />
    </div>
  </div>
</template>

<script>

import MeBlock from './components/MeBlock.vue'
import ExperienceBlock from './components/ExperienceBlock.vue'

export default {
  name: 'App',
  components: {
    MeBlock,
    ExperienceBlock
  },
}

</script>

<style lang="scss">
  @import "../public/assets/css/const";

  #app {
    font-family:  'Courier New', monospace, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    background-color: $default-color;
  }

  #container-app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    height: 100vh;
    width: 100vw;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    border-radius: unset;
  }




</style>
