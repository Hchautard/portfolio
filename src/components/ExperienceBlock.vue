<template>
    <div id="experience">
        <div id="container-experience" class="neomorphic">
            <h1>{{ message }}</h1>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ExperienceBlock',
    data() {
        return {
            message: 'Hello Vue!'
        }
    },
}
</script>

<style>
    #me {
        font-family:  'Courier New', monospace, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }

    #container-me {
        display: flex;
        justify-content: center;
        align-items: center;
        height: auto;
        width: 50vh;
        height: 20vh;
    }

</style>