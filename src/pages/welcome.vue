<template>
    <section class="welcome">
    </section>
</template>

<script>
import $ from 'jquery'
    export default{

        mounted() {
            this.setFullscreen();
            this.init();
        },

        methods: {

            setFullscreen() {
                $('section.welcome').height($(window).height());
            },

            init() {
                this.$store.dispatch('setArticleDetail', false);
            }
        }
    }
</script>

<style lang="less">
    section.welcome{
        width: 100%;
        background-image: url(../images/Shapes.jpg);
        background-size: cover;
        background-position: center center;
        background-repeat:  no-repeat;
    }
</style>