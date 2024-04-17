<template>
    <div id="my-skill">
        <h1>Mes compétences</h1>
        <div id="skill-section">
            <div id="skill-text">
                <h3>Front-end</h3>
                <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis reiciendis aut accusantium quaerat alias explicabo doloribus sapiente, dolorum cum numquam nobis debitis, quidem vitae obcaecati dicta corporis aliquid adipisci earum.
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Laudantium doloremque veritatis vel reiciendis pariatur, quibusdam unde! Voluptatum, culpa vero? Cum reprehenderit quaerat necessitatibus nam officiis nostrum odio hic doloremque pariatur!
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MySkills',
}
</script>

<style lang="scss" scoped>
    @import "../../public/assets/css/const.scss";

    #my-skill {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        margin: 100px;
    }
</style>