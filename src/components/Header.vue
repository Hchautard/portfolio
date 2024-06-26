<template>
  <header>
    <nav class="sublinks">
        <div class="me-title">
            <h3><a href="#about-me">Moi</a></h3>
        </div>
        <div class="project-title">
            <h3><a href="#my-projects">Mes projets</a></h3>
        </div>
        <div class="contact-title">
            <h3><a href="#contact">Me contacter</a></h3>
        </div>
    </nav>
   
        <a href="https://github.com/SuhDud3"> 
            <i class="fa fa-github" style="font-size:36px"></i>
        </a>
    
</header>
</template>

<script>
export default {
  name: 'HeaderPort',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
    @import "../../public/assets/css/const";

    .sublinks {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: right;
        width: 25em;
    }

    header {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
        height: 975px;
        margin-bottom: 50px;

        box-sizing: border-box;
        -moz-box-sizing: border-box;
        -webkit-box-sizing: border-box;
    }

    * {
        color: $darkColor;
    }
</style>
