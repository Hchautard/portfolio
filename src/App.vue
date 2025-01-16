<template>
    <div class="bg-gray-50 py-24 sm:py-32">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <MeBlock />
                <ExperienceBlock />
            </div>
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
    ExperienceBlock,
  },
}

</script>

<style lang="scss">
  @import './index.css';
  @import "../public/assets/css/const";

  #app {
    font-family:  'Courier New', monospace, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    background-color: $default-color;
  }

  #container-app {
    display: grid;
    grid-template-columns: 3fr 2fr;
    height: 90%;
    width: 90%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    border-radius: unset;
    
    background-color: red;
  }




</style>
