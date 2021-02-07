<template>
    <div id="nav">
        <Navigation />
    </div>

    <template v-if="program === 'fitness'">
        <div class="programs">
            <h1>Programs</h1>
            <div class="background-container">
                <div>
                    Remote Coaching: Programming delivered to you from Agoge
                    Strong Performance Training that is focused to your goals.
                    No templates or cookie cutter programs. Our programs are
                    focused on your strengths, weaknesses and desires for
                    physical fitness. You will get consistent communication with
                    our head coach, with technique, mindset and motivational
                    coaching to help you maximize your results.Remote Coaching:
                    Programming delivered to you from Agoge Strong Performance
                    Training that is focused to your goals. No templates or
                    cookie cutter programs. Our programs are focused on your
                    strengths, weaknesses and desires for physical fitness. You
                    will get consistent communication with our head coach, with
                    technique, mindset and motivational coaching to help you
                    maximize your results.
                </div>
                <div>
                    Personal Training/Small Group Training: In person training
                    at our private studio with our head coach. As always, no
                    templates or cookie cutter programs. Our programs are always
                    focused on your strengths, weaknesses and desires for
                    physical fitness. If you have friends that you want to train
                    with group discounts are available making personal training
                    more fun, enjoyable and motivating at a great rates.
                </div>

                <h3>Rates/Specials</h3>

                <div>
                    Philosophy: At Agoge Strong Performance Training we utilize
                    a combination different training modalities in order to
                    deliver results including aerobic & anaerobic conditioning,
                    strength, flexibility, balance, coordination, core, and
                    power training methods. Your program will be designed and
                    delivered to you in a way that it is challenging yet not
                    intimidating or boring. No matter what your fitness status
                    is we can tailor it to your needs.
                </div>
                <div>
                    Aesthetics: If you are looking to look good, gain muscle and
                    lose fat our aesthetics program is for you. We use a
                    combination of bodybuilding and functional fitness
                    approaches in order to gain muscle and lose fat and help you
                    gain that beach body you always wanted.
                </div>
                <div>
                    Functional Fitness: A combination of our health and fitness
                    training approach we will combine aerobic & anaerobic
                    conditioning, strength, flexibility, balance, coordination,
                    core, and power training methods to get you results.
                    Programs are broken into a combination of strength and
                    fitness development and high intensity workouts using
                    functional movements such as squat, deadlift, bench press,
                    overhead press, Olympic lifts (snatch and clean & jerk),
                    gymnastics movements and aerobic methods such as rowing,
                    biking, running and jump rope. This type of training brings
                    great results with a challenging and fun approach that keeps
                    people coming back for more.
                </div>

                <h3>Performance</h3>

                <div>
                    Sport Performance: Training and Programming focused on
                    developing specific attributes for the sport you play,
                    including sport specific strength, power, injury prevention
                    and conditioning.
                </div>
                <div>
                    Speed Development: Free of cost to any sport performance
                    client, speed development programming and training breaks
                    down the mechanics of acceleration, top end speed, change of
                    direction, agility, reactions and change of direction in
                    order to maximize your game speed and make you into the
                    lethal athlete you desire.
                </div>
                <div>
                    Olympic Weightlifting: Learn and develop into a confident,
                    weightlifting athlete. Learn and develop your skills in the
                    Snatch and the Clean & Jerk using a variety of skills and
                    drills in order to maximize your abilities in the two
                    Olympic lifts.
                </div>
                <div>
                    Powerlifting: Programming focusing on maxing your abilities
                    within the Squat, Bench Press and Deadlift. If you want to
                    focus on maximizing your overall strength this program is
                    what you want.
                </div>
            </div>
        </div>
    </template>
    <template v-else>
        <h1>SPORTS</h1>
    </template>
</template>

<style lang="scss" scoped>
.programs {
    padding: 0 2rem;

    .background-container {
        background-color: rgba(0, 0, 0, 0.5);
    }
}
</style>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Navigation from '@/components/Navigation.vue'; // @ is an alias to /src

@Options({
    data() {
        return {
            program: this.$route.params.program
        };
    },

    components: {
        Navigation
    }
})
export default class About extends Vue {}
</script>
