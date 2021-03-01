<template>
    <div id="nav">
        <Navigation />
    </div>

    <div class="program-options">
        <label
            :class="{ selected: isFitnessSelected }"
            @click="setProgram('fitness')"
            >Fitness & Health</label
        >
        <label
            :class="{ selected: isPerformanceSelected }"
            @click="setProgram('performance')"
            >Performance</label
        >
        <label
            :class="{ selected: isRatesSelected }"
            @click="setProgram('rates')"
            >Rates & Services</label
        >
    </div>

    <template v-if="program === 'fitness'">
        <div class="program-info">
            <div class="background-container">
                <div class="bullet">
                    <b>General Health & Fitness: </b> If you simply want to feel
                    better, look better and lead a healthier life, a general
                    approach to fitness is probably what you are looking for.
                    Pulling from numerous training methodologies and experience
                    we can set-up a program for you that is both exciting and
                    effective without all the nuances of the specific training
                    programs that we offer.
                </div>

                <div class="bullet">
                    <b>Functional Fitness: </b> A combination of our health and
                    fitness training approach we will combine aerobic &
                    anaerobic conditioning, strength, flexibility, balance,
                    coordination, core, and power training methods to get you
                    results. Programs are broken into a combination of strength
                    and fitness development and high intensity workouts using
                    functional movements such as squat, deadlift, bench press,
                    overhead press, Olympic lifts (snatch and clean & jerk),
                    gymnastics movements and aerobic methods such as rowing,
                    biking, running and jump rope. This type of training brings
                    great results with a challenging and fun approach that keeps
                    people coming back for more.
                </div>

                <div class="bullet">
                    <b>Aesthetics: </b> If you are looking to look good, gain
                    muscle and lose fat our aesthetics program is for you. We
                    use a combination of bodybuilding and functional fitness
                    approaches in order to gain muscle and lose fat and help you
                    gain that beach body you always wanted.
                </div>
            </div>
        </div>
    </template>
    <template v-else-if="program === 'performance'">
        <div class="program-info">
            <div class="background-container">
                <div class="bullet">
                    <b>Sport Performance: </b> Whether you would like to train
                    like an athlete or focus on developing specific attributes
                    for the sport you play, including sport specific strength,
                    power, injury prevention and conditioning. Using scientific
                    backed training methods, we apply a periodized approach to
                    developing strength, speed and power that works with one
                    another to provide a progressive program that will take you
                    into your season bigger, faster and stronger.
                </div>

                <div class="bullet">
                    <b>Speed Development: </b> Free of cost to any sport
                    performance client, speed development programming and
                    training breaks down the mechanics of acceleration, top end
                    speed, change of direction, agility, reactions and change of
                    direction in order to maximize your game speed and make you
                    into the lethal athlete you desire.
                </div>

                <div class="bullet">
                    <b>Functional Fitness Competitor: </b> Using the principles
                    of functional fitness, the functional fitness competitor
                    programming includes high level conditioning, skills and
                    strength programming into one to make you the best
                    all-around fitness competitor you can be.
                </div>

                <div class="bullet">
                    <b>Olympic Weightlifting: </b> Learn and develop into a
                    confident, weightlifting athlete. Learn and develop your
                    skills in the Snatch and the Clean & Jerk using a variety of
                    skills and drills in order to maximize your abilities in the
                    two Olympic lifts.
                </div>

                <div class="bullet">
                    <b>Powerlifting: </b> Programming focusing on maxing your
                    abilities within the Squat, Bench Press and Deadlift. If you
                    want to focus on maximizing your overall strength this
                    program is what you want.
                </div>
            </div>
        </div>
    </template>
    <template v-else-if="program === 'rates'">
        <div class="program-info">
            <div class="background-container">
                <div class="bullet"><b>Rates: </b> Show me the money.</div>
            </div>
        </div>
    </template>
</template>

<style lang="scss" scoped>
.program-options {
    label {
        color: #b86410;
        font-weight: 400;
        font-size: 2rem;
        padding: 1rem 3rem;
        cursor: pointer;
        text-decoration: none;

        &.selected {
            text-decoration: underline;
        }
    }
}

.program-info {
    margin: 0 15% 3% 15%;
    overflow: scroll;

    .background-container {
        background-color: rgba(0, 0, 0, 0.7);
        border-radius: 10px;

        .bullet {
            padding: 1rem 0.5rem;
            font-size: 1.5rem;
        }
    }
}
</style>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Navigation from '@/components/Navigation.vue'; // @ is an alias to /src

@Options({
    data() {
        return {
            program: this.$route.params.program || 'fitness'
        };
    },
    methods: {
        setProgram(programName: string) {
            this.program = programName;
        }
    },
    computed: {
        isFitnessSelected() {
            return this.program === 'fitness';
        },
        isPerformanceSelected() {
            return this.program === 'performance';
        },
        isRatesSelected() {
            return this.program === 'rates';
        }
    },
    components: {
        Navigation
    }
})
export default class About extends Vue {}
</script>
