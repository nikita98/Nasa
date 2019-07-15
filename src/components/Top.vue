<template>
    <div class="top">
        <top-nav
                :sections="[
                ['MISSIONS', ['International Space Station', 'Curiosity Rover', 'Hubble Space Telescope', 'Parker Solar Probe']],
                ['NEWS', ['a', 'b']],
                ['NASA TV', ['International Space Station', 'Curiosity Rover', 'Hubble Space Telescope', 'Parker Solar Probe']],
                ['galleries', ['International Space Station', 'Curiosity Rover', 'Hubble Space Telescope', 'Parker Solar Probe']],
                ['AAA', ['a', 'b']],
                ['SHUTTLES', ['a', 'b']],
                ['NASA FOR CHILDREN', ['International Space Station', 'Curiosity Rover', 'Hubble Space Telescope', 'Parker Solar Probe']],
                ['EVENTs', ['a', 'b', 'c', 'd', 'e']],
                ]"/>
        <div class="top__social-wrap">
            <social />
        </div>
    </div>
</template>

<script>
    import TopNav from './TopNav.vue'
    import Social from './Social.vue'

    export default {
        components: {
            TopNav,
            Social
        }
    }
</script>

<style scoped lang="scss">
    .top {
        height: 100vh;
        background-image: linear-gradient(179.77deg, rgba(37, 40, 42, 0) 50.79%, #252525 98.57%),
        repeating-linear-gradient(90deg, rgba(#fff, 0), rgba(#fff, 0) 174px, rgba(#fff, 0.3) 1px, rgba(#fff, 0.3) 175px),
        repeating-linear-gradient(1800deg, rgba(#fff, 0), rgba(#fff, 0) 174px, rgba(#fff, 0.3) 1px, rgba(#fff, 0.3) 175px),
        url(../assets/cosmonaut.jpg);
        background-size: cover;
        &__social-wrap{
            position: absolute;
            right: 0;
            top: 50%;
            transform: translateY(-50%);
        }
    }
</style>
