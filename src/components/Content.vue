<template>
    <div class="content">
        <calendar/>
        <flies/>
        <lurk-buttons/>
    </div>
</template>

<script>
    import calendar from './Calendar.vue'
    import flies from './Flies.vue'
    import LurkButtons from './LurkButtons.vue'
    export default {
        components: {
            calendar,
            flies,
            'lurk-buttons': LurkButtons
        }
    }
</script>

<style scoped lang="scss">
    .content {
        overflow: hidden;
        position: relative;
        padding: 200px 100px;
        display: flex;
        justify-content: space-around;
        &__flies{
            margin-left: 2%;
        }
        &__lurk-buttons{
            left: 1%;
            top: 300px;
        }
    }
</style>
