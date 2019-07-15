<template>
    <div class="lurk-buttons content__lurk-buttons">
        <div class="lurk-buttons__lurk-button">
            TOP-10
        </div>
        <div class="lurk-buttons__lurk-button">
            TWEETS
        </div>
        <div class="lurk-buttons__lurk-button">
            <div class="lurk-buttons__i"></div>
            LIVE
        </div>
        <div class="lurk-buttons__lurk-button">
            EVENTS
        </div>
    </div>

</template>

<script>
</script>

<style scoped lang="scss">
    .lurk-buttons {
        position: absolute;
        &__lurk-button{
            text-transform: uppercase;
            font-size: 14px;
            display: flex;
            align-items: center;
            justify-content: space-around;
            font-weight: 200;
            background: #191919;
            border: 1px solid rgba(255,255,255,0.3);
            border-radius: 8px;
            padding: 4px 5px;
            margin: 10px;
        }
        &__i{
            display: inline-block;
            width: 7px;
            height: 7px;
            border-radius: 50%;
            background: #FF0000;
        }
    }
</style>
