<template>
    <div class="social">
        <div class="social__wrap">
            <a href="#" class="social__item">
                <div class="icon social__icon">
                    <img src="../assets/facebook.png" alt="" class="icon__img">
                </div>
            </a>
            <a href="#" class="social__item">
                <div class="icon social__icon">
                    <img src="../assets/pinterest.png" alt="" class="icon__img">
                </div>
            </a>
            <a href="#" class="social__item active">
                <div class="icon social__icon">
                    <img src="../assets/share.svg" alt="" class="icon__img ">
                </div>
            </a>
            <a href="#" class="social__item">
                <div class="icon social__icon">
                    <img src="../assets/google-plus.png" alt="" class="icon__img">
                </div>
            </a>
            <a href="#" class="social__item">
                <div class="icon social__icon">
                    <img src="../assets/instagram.png" alt="" class="icon__img">
                </div>
            </a>
            <a href="#" class="social__item">
                <div class="icon social__icon">
                    <img src="../assets/twitter.png" alt="" class="icon__img">
                </div>
            </a>
            <a href="#" class="social__item">
                <div class="icon social__icon">
                    <img src="../assets/youtube.png" alt="" class="icon__img">
                </div>
            </a>
        </div>
    </div>
</template>

<script>
    export default {}
</script>

<style scoped lang="scss">
    .social {
        &__item {
            display: block;
            padding: 7px 5px;
            margin: 17px 0;
            width: 110px;
            border-radius: 10px 0 0 10px;

            &.active {
                background-color: #91F9FA;

                .icon {
                    filter: invert(0);
                }
            }

            &:hover {
                background-color: #91F9FA;

                .icon {
                    filter: invert(0);
                }
            }
        }
    }
</style>

