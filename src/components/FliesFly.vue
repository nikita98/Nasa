<template>
    <div class="flies-fly">
        <div class="flies-fly__title">
            {{title}}
        </div>
        <div class="flies-fly__text">
            {{text}}
        </div>
    </div>
</template>

<script>
    export default {
        props:{
            title: '',
            text: ''
        }
    }
</script>

<style scoped lang="scss">
    .flies-fly{
        text-align: left;
        font-weight: 300;
        padding-bottom: 20px;
        margin-bottom: 25px;
        margin-right: 25px;
        border-bottom: 1px solid rgba(255,255,255,0.3);
        &__title{
            font-weight: 500;
            font-size: 30px;
            margin-bottom: 22px;
        }
    }
</style>