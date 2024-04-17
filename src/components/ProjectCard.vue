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
                <h3>{{ projects.title }}</h3><br/>
                <p>{{ projects.description }}</p><br/>
                <a :href="projects.github" target="_blank">Voir le GitHub</a><br/>
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

        &:hover {
            cursor: pointer;
            .modal {
                transition: 0.5s;

                height: 700px;
                width: 1500px;

                .modal-content {
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    height: 100%;
                    width: 100%;
                }


                display: block;
                position: fixed;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                background-color: white;
                border: 1px solid black;
                padding: 20px;
                z-index: 1000;

                .modal-technologies {
                    display: flex;
                    flex-direction: row;
                    justify-content: center;
                    align-items: center;
                    padding-top: 10px;
                    width: 200px;
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
    }


</style>