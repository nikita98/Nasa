<template>
    <div class="top-nav">
        <a href="#" class="logo"><img class="logo__img" src="../assets/logo.png" alt=""></a>
        <ul class="top-nav__list">
            <li class="top-nav__item" v-for="(section, index) in sections" v-bind:key="index">
                <div class="top-nav__title">
                    <a href="#">{{section[0]}}</a>
                </div>
                <div class="top-nav__dropdown">
                    <ul class="top-nav__dropdown-list">
                        <li class="top-nav__dropdown-item" v-for="(topic, index) in section[1]" v-bind:key="index">
                            <a class="top-nav__link" href="#">{{topic}}</a>
                        </li>
                    </ul>
                    <div class="top-nav__arrow"></div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: {
            sections: {name: '', topics: {}}
        }
    }
</script>

<style scoped lang="scss">
    .top-nav {
        display: flex;
        justify-content: center;
        align-items: flex-start;
        padding-top: 45px;

        &__link {
            color: #969696;
            display: block;
            padding: 6px 10px;
            font-weight: 300;
            &:hover {
                color: #91F9FA;
            }
        }

        &__list {
            padding-top: 25px;
            list-style: none;
            display: flex;
            align-items: flex-start;
            flex-wrap: nowrap;
            font-size: 15px;
            width: 1200px;
            max-width: 80%;
        }

        &__item {
            width: 100%;
            border-radius: 13px;
            &:hover{
                transition: 0.3s;
                background-color: rgba(#000, 0.6);
                animation-timing-function: ease;
            }
            &:hover > .top-nav__dropdown {
                max-height: 500px;
                opacity: 1;
            }
        }

        &__title {
            text-transform: uppercase;
            padding: 12px 10px;
        }

        &__dropdown {
            max-height: 0px;
            opacity: 0;
            transition: 0.3s;
            animation-timing-function: ease;
            overflow: hidden;
        }

        &__dropdown-item {
            list-style: none;
        }

        &__arrow {
            width: 20px;
            height: 20px;
            margin: 10px auto 20px;
            transform: rotate(45deg);
            border-bottom: 1px solid #969696;
            border-right: 1px solid #969696;
            cursor: pointer;

            &:hover {
                border-bottom: 1px solid #91F9FA;
                border-right: 1px solid #91F9FA;
            }
        }
    }
</style>
