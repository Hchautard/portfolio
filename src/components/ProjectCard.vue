<template>
    <div class="projects-card">
        <h3 class="projects-title">{{ projects.title }}</h3>
        <div v-if="projects.image" class="projects-img">
            <img :src="projects.image" alt="image du projet">
        </div>
        <div v-if="projects.link" class="projects-link">
            <a :href="projects.link" target="_blank">Voir le projet</a>
        </div>

        <div v-if="projects.github" class="projects-github">
            <a :href="projects.github" target="_blank">Voir le code source</a>
        </div>

        <div class="modal" v-if="projects.modal">
            <div class="modal-content">
                <h3 class="modal-project-title">{{ projects.title }}</h3>
                <p>{{ projects.description }}</p>
                <div class="modal-technologies">
                    <p v-for="technologies in projects.technologies" :key="technologies.id">{{ technologies }}</p>
                </div>
                <CarouselImageContent :image_content="projects.image_content"/>
            </div>
        </div>
    </div>
    
</template>

<script>
import CarouselImageContent from './CarouselImageContent.vue'

export default {
    name: 'ProjectCard',
    props: {
        projects: Object,
    },
    components: {
        CarouselImageContent
    },
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
      @import "../../public/assets/css/const.scss";

    .projects-card {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        height: 100%;
        background-color: $white;
        border-radius: 20px;

        

        &:hover {
            cursor: pointer;

            .modal {

                height: 700px;
                width: 1500px;

                .modal-project-title {
                    font-size: 1.5em;
                    font-family: 'Notted';
                    color: $darkDarkColor;
                }

                .modal-content {
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    height: 100%;
                    width: 100%;

                    p {
                        width: 80%;
                        font-family: monospace;
                        font-size: 1.5em;
                        font-weight: 300;
                        color: $darkDarkColor;
                        text-align: justify;
                        line-height: 1.5em;
                    }
                }

                
                    display: block;
                    position: fixed;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    background-color: $white;
                    border-radius: 20px;
                    padding: 20px;
                    z-index: 1000;
                

                

                .modal-technologies {
                    display: flex;
                    flex-direction: row;
                    width: 50%;
                    margin-top: -20px;

                    p {
                        text-align: center;
                    }
                }
            }
        }
    }

    img {
        width: 350px;
    }

    .projects-title {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        width: auto;
        padding: 0px 20px;
        font-family: 'Notted';
        font-size: 1.5em;
        color: $darkDarkColor;
    }

    .projects-img {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .projects-description {
        display: flex;
        justify-content: center;
        align-items: center;
        width: auto;
        font-size: 1em;
        padding-right: 15px;
        padding-left: 15px;
        padding-top: 10px;
    }

    .modal {
        display: none;
        transition: 1s;
    }


</style>