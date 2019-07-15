<template>
    <div class="calendar-date">
        <div class="calendar-date__title"
             @click="(date || text) ? (active = !active) : ''"
             :class="{'calendar-date__title_clickable': (date || text)}">
            <div class="calendar-date__title-after"
                 :class="{'calendar-date__title-after_active': active}"></div>
            <div class="calendar-date__title-text"
                 :class="{'calendar-date__title-text_not-bright': notBright}">
                {{title}}
            </div>
            <div class="calendar-date__i" v-if="date || text"
                 :class="{'calendar-date__i_active': active}"></div>
        </div>
        <transition name="" v-show="active">
            <div class="calendar-date__body"
                 v-if="date || text"
                 :class="{'calendar-date__body_active': active}">
                <div class="calendar-date__body-item">
                    <div class="calendar-date__date">
                        {{date}}
                    </div>
                    <div class="calendar-date__msg">
                        {{text}}
                    </div>
                </div>
            </div>
        </transition>
    </div>
</template>

<script>
    export default {
        props: {
            title: String,
            text: String,
            date: String,
            notBright: ''
        },
        data(){
            return{
                active: false
            }
        }
    }
</script>

<style scoped lang="scss">
    .calendar-date {
        width: 100%;
        height: 140px;
        position: relative;

        &:not(:last-child) {
            border-right: 0.3px solid rgba(#fff, 0.7);

            &:after {
                content: '';
                position: absolute;
                right: 0;
                bottom: 0;
                transform: translate(50%, 50%);
                background-color: rgba(#fff, 0.7);
                height: 3px;
                width: 3px;
                border-radius: 100%;
            }
        }

        &__title {
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;

            &_clickable {
                cursor: pointer;
            }
        }

        &__title-text {
            z-index: 1;
            &_not-bright{
               opacity: 0.6;
            }
        }

        &__title-after {
            position: absolute;
            bottom: 2px;
            height: 70%;
            border-radius: 26px 26px 0 0;
            z-index: 0;
            width: 40%;
            background-color: #2A478A;
            opacity: 0;
            transition: 0.3s;
            &_active{
                opacity: 1;
            }
        }

        &__i {
            position: absolute;
            z-index: 100;
            height: 11px;
            width: 11px;
            border-radius: 50%;
            bottom: 20px;
            background: rgba(255, 10, 10, 0.7);
            transition: 0.5s;
            animation-timing-function: ease;
            &_active{
                bottom: -60px;
            }
        }

        &__body {
            position: absolute;
            left: 30%;
            top: 137px;
            z-index: 2;
            padding: 44px 20px 30px 25px;
            text-align: left;
            background: #2A478A;
            border-radius: 0 26px 26px 26px;
            width: 450px;
            font-size: 21px;
            line-height: 1.3em;
            font-weight: 200;
            color: #fff;
            transition: 0.3s;
            opacity: 0;
            &_active{
                opacity: 1;
            }
        }
        &__date{
            margin-left: 30px;
            margin-bottom: 30px;
        }
    }
</style>
