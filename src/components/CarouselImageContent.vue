<template>
    <div class="carousel-image-content">
        <button @click="previousImage">&lt;</button>
            <Transition name="slide-fade">
                <img :src="image_content[currentImageIndex]" alt="image du projet" v-if="show">
            </Transition>
        <button @click="nextImage">&gt;</button>
    </div>
</template>

<script>

export default {
    name: 'CarouselImageContent',
    props: {
        image_content: Array,
    },
    data() {
        return {
            currentImageIndex: 0,
            show: true
        }
    },

    methods: {
        nextImage() {
            this.currentImageIndex++;
            if (this.currentImageIndex >= this.image_content.length) {
                this.currentImageIndex = 0;
            }
            this.show = false;
            this.$nextTick(() => {
                this.show = true;
            });
        },
        previousImage() {
            this.currentImageIndex--;
            if (this.currentImageIndex < 0) {
                this.currentImageIndex = this.image_content.length - 1;
            }
            this.show = false;
            this.$nextTick(() => {
                this.show = true;
            });
        }
    }
}

</script>

<style lang="scss" scoped>
    @import "../../public/assets/css/const.scss";

    .slide-fade-enter-active {
        transition: all 0.3s ease-out;
        }

        .slide-fade-leave-active {
        transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
        }

        .slide-fade-enter-from,
        .slide-fade-leave-to {
        transform: translateX(20px);
        opacity: 0;
        }

    .carousel-image-content {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }

    img {
        width: 50%;
    }

    button {
        background-color: red;
        color: white;
        border: none;
        padding: 10px;
        margin: 50px;
        width: 40px;
        cursor: pointer;
    }
    button:hover {
        background-color: blue;
    }

</style>