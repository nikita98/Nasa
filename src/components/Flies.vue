<template>
    <div class="flies content__flies">
        <h3 class="flies__title">LAUNCH AND LANDINGS</h3>
        <div class="flies__list">
            <flies-fly
                    title="Tuesday, feb. 19"
                    text="Launch of Israeli lunar lander"
            />
            <flies-fly
                    title="Monday, mar. 25"
                    text="Launch of ISRO (India) lunar orbiter, lander, and rover"
            />
            <flies-fly
                    title="September 2019"
                    text="Sample collection from asteroid Bennu"
            />
            <flies-fly
                    title="Late 2019"
                    text="Launch of Chinese lunar sample return mission"
            />
            <flies-fly
                    title="July 2020"
                    text="Launch of ESA Mars rover and Russian surface platform"
            />
        </div>
        <div class="flies__image">
            <img src="../assets/purepng.png" alt="purepng">
        </div>
    </div>

</template>

<script>
    import FliesFly from './FliesFly.vue'

    export default {
        components: {
            'flies-fly': FliesFly
        }
    }
</script>

<style scoped lang="scss">
    .flies {
        position: relative;
        width: 500px;
        background: #3355A3;
        padding: 50px 30px 330px 60px;
        &__title{
            margin-bottom: 150px;
        }
        &__image{
            position: absolute;
            bottom: 70px;
            left: 45%;
        }
    }
</style>
