<template>
    <div id="nav">
        <Navigation />
    </div>

    <div class="about-options">
        <label
            :class="{ selected: isAgogeSelected }"
            @click="setOption('agoge')"
            >Agoge</label
        >
        <label
            :class="{ selected: isHeadCoachSelected }"
            @click="setOption('headCoach')"
            >Head Coach</label
        >
        <label
            :class="{ selected: isFacilitySelected }"
            @click="setOption('facility')"
            >Facility</label
        >
        <label
            :class="{ selected: isTestimonialsSelected }"
            @click="setOption('testimonials')"
            >Testimonials</label
        >
    </div>

    <template v-if="program === 'agoge'">
        <div class="about">
            <div class="background-container">
                <div class="bullet">
                    Agoge Strong Performance Training provides both in-person
                    and remote coaching for individuals looking to get the most
                    out of their life. Whether you are trying to increase
                    performance for your sport or if you are trying to lead a
                    healthier life our highly experienced staff will tailor an
                    approach to meet your goals. Agoge Strong has a philosophy
                    that a fitness programs success is based on not only the
                    coach to client relationship but also the teaching of the
                    core values of Agoge Strong. Bringing your best Effort,
                    Consistently with a positive Attitude where you are willing
                    to gain Knowledge about what you are trying to accomplish
                    will nearly always guarantee results and accomplishment of
                    your goals. Our mission at Agoge Strong is to help anyone
                    and everyone reach their full potential, not only within the
                    realm of physical fitness but in every aspect of life.
                    Leaning on our core values we believe that the lessons
                    learned with us will resonate beyond the gym and your
                    fitness and help you be successful in all walks of life. We
                    look to continuously grow and serve the community of
                    Southern Maryland and abroad. At strive to help bring more
                    opportunities for the youth athletes that are currently
                    underserved in the area, to develop into strong athletes of
                    their sport.
                </div>
            </div>
        </div>
    </template>
    <template v-else-if="program === 'headCoach'">
        <div class="about">
            <div class="background-container">
                <img alt="Mat Strong" src="../assets/mat.jpg" />

                <div class="bullet">
                    Head Coach Mat Strong has a variety of experience to pull
                    from in order to help you meet your goals. Mat has
                    experience as a collegiate athlete, being a long-time soccer
                    player as well experience in football, baseball, basketball
                    and track and field. This experience is leaned on to know
                    the demands of the sports that athletes & clients are
                    performing in. Numerous years of sport coaching, functional
                    fitness coaching and experience working with sport
                    nutrition, sport science and strength and conditioning teams
                    at University of Maryland has brought our Head Coach to the
                    point of opening Agoge Strong Performance Training. Mat
                    Strong hold certifications and specializes in Functional
                    Fitness, Sport Performance, Speed and Power Development, &
                    Olympic Weightlifting. Mat also focused his undergrad
                    studies on sport psychology studying how psychological
                    skills training can help develop higher levels of
                    performance as well as be a preventative measure against
                    mental illness.
                </div>
                <div>
                    Credentials:B.S. Kinesiology University of
                    MarylandNSCA-CSCSUSAW- Sport Performance CoachCrossFit
                    Level-1NASE-CSS Level II NSPA-CCSUS Soccer- E
                    LiscenseCurrently Studying for M.S. in Human Performance and
                    Injury Prevention
                </div>
            </div>
        </div>
    </template>
    <template v-else-if="program === 'facility'">
        <div class="about">
            <div class="background-container">
                <h3>Facilities</h3>

                <div>
                    Private Facility: Our private performance center provides
                    any client the opportunity to train in peace without
                    interruption that you would get in a large commercial gym.
                    Our facility provides our clients with all the tools they
                    will need in order to reach their goals:
                </div>
                <div>Photos: TODO</div>
            </div>
        </div>
    </template>
    <template v-else-if="program === 'testimonials'">
        <div class="about">
            <div class="background-container">
                <h1>todo</h1>
            </div>
        </div>
    </template>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Navigation from '@/components/Navigation.vue'; // @ is an alias to /src

@Options({
    data() {
        return {
            program: this.$route.params.program || 'agoge'
        };
    },
    methods: {
        setOption(programName: string) {
            this.program = programName;
        }
    },
    computed: {
        isAgogeSelected() {
            return this.program === 'agoge';
        },
        isHeadCoachSelected() {
            return this.program === 'headCoach';
        },
        isFacilitySelected() {
            return this.program === 'facility';
        },
        isTestimonialsSelected() {
            return this.program === 'testimonials';
        }
    },
    components: {
        Navigation
    }
})
export default class About extends Vue {}
</script>

<style lang="scss" scoped>
.about-options {
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

.about {
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
