<template>
    <div class="calendar">
        <h3 class="calendar__title">
            <div>NASA EVENT CALENDAR</div>
            <div>FEBRUARY 2019</div>
        </h3>
        <div class="calendar__grid">
            <div class="calendar__week">
                <calendar-date title="SUN"/>
                <calendar-date title="MON"/>
                <calendar-date title="TUE"/>
                <calendar-date title="WED"/>
                <calendar-date title="THU"/>
                <calendar-date title="FRI"/>
                <calendar-date title="SAT"/>
            </div>
            <div class="calendar__week">
                <calendar-date title="28" notBright="true"/>
                <calendar-date title="29" notBright="true"/>
                <calendar-date title="30" notBright="true"/>
                <calendar-date title="31" notBright="true"
                              date="Jun.31, 2019 7:00 p.m. - 10:00 p.m."
                              text="The NASA Wallops Flight Facility Visitor Center and its partner the Delmarva Space Sciences Foundation will host an Astronomy night from 7 to 10 p.m. on Friday, March 15, featuring Earth’s Moon and Apollo’s 50th Anniversary."
                />
                <calendar-date title="1"></calendar-date>
                <calendar-date title="2"></calendar-date>
                <calendar-date title="3"></calendar-date>
            </div>
            <div class="calendar__week">
                <calendar-date title="4"></calendar-date>
                <calendar-date title="5"></calendar-date>
                <calendar-date title="6"></calendar-date>
                <calendar-date title="7"></calendar-date>
                <calendar-date title="8"></calendar-date>
                <calendar-date title="9"></calendar-date>
                <calendar-date title="10"></calendar-date>
            </div>
           <div class="calendar__week">
               <calendar-date title="11"></calendar-date>
               <calendar-date title="12"></calendar-date>
               <calendar-date title="13"></calendar-date>
               <calendar-date title="14"></calendar-date>
               <calendar-date title="15"></calendar-date>
               <calendar-date title="16"></calendar-date>
               <calendar-date title="17"></calendar-date>
           </div>
            <div class="calendar__week">
                <calendar-date title="18"></calendar-date>
                <calendar-date title="19"
                               date="Jun.31, 2019 7:00 p.m. - 10:00 p.m."
                               text="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur aut corporis delectus eligendi est, iusto maxime recusandae tempore voluptas voluptatum."
                ></calendar-date>
                <calendar-date title="20"
                               date="Jun.31, 2019 7:00 p.m. - 10:00 p.m."
                               text="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur aut corporis delectus eligendi est, iusto maxime recusandae tempore voluptas voluptatum."
                ></calendar-date>
                <calendar-date title="21"></calendar-date>
                <calendar-date title="22"></calendar-date>
                <calendar-date title="23"></calendar-date>
                <calendar-date title="24"></calendar-date>
            </div>
            <div class="calendar__week">
                <calendar-date title="25"></calendar-date>
                <calendar-date title="26"></calendar-date>
                <calendar-date title="27"></calendar-date>
                <calendar-date title="28"></calendar-date>
                <calendar-date title="1" notBright="true"></calendar-date>
                <calendar-date title="2" notBright="true"></calendar-date>
                <calendar-date title="3" notBright="true"></calendar-date>
            </div>
        </div>
    </div>
</template>

<script>
    import CalendarDate from './CalendarDate.vue'

    export default {
        components: {
            'calendar-date': CalendarDate
        }
    }
</script>

<style scoped lang="scss">
    .calendar {
        width: 1053px;
        background: #3355A3;
        padding-top: 80px;

        &__title {
            display: flex;
            justify-content: space-between;
            margin: 0 69px 90px 44px;
        }

        &__grid {
            width: 100%;
        }

        &__week {
            display: flex;

            &:not(:last-child) {
                border-bottom: 0.3px solid rgba(#fff, 0.7);
            }

            &:last-child {
                .calendar-date:after {
                    content: none;
                }
            }
        }
    }
</style>
