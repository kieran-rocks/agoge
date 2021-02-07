<template>
    <div id="nav">
        <Navigation />
    </div>

    <div class="background-container">
        <ul>
            <div>
                Agoge Strong Performance Training provides both in-person and
                remote coaching for individuals looking to get the most out of
                their life. Whether you are trying to increase performance for
                your sport or if you are trying to lead a healthier life our
                highly experienced staff will tailor an approach to meet your
                goals. Agoge Strong has a philosophy that a fitness programs
                success is based on not only the coach to client relationship
                but also the teaching of the core values of Agoge Strong.
                Bringing your best Effort, Consistently with a positive Attitude
                where you are willing to gain Knowledge about what you are
                trying to accomplish will nearly always guarantee results and
                accomplishment of your goals. Our mission at Agoge Strong is to
                help anyone and everyone reach their full potential, not only
                within the realm of physical fitness but in every aspect of
                life. Leaning on our core values we believe that the lessons
                learned with us will resonate beyond the gym and your fitness
                and help you be successful in all walks of life. We look to
                continuously grow and serve the community of Southern Maryland
                and abroad. At strive to help bring more opportunities for the
                youth athletes that are currently underserved in the area, to
                develop into strong athletes of their sport.
            </div>

            <h3>Facilities</h3>

            <div>
                Private Facility: Our private performance center provides any
                client the opportunity to train in peace without interruption
                that you would get in a large commercial gym. Our facility
                provides our clients with all the tools they will need in order
                to reach their goals:
            </div>
            <div>Photos: TODO</div>

            <h3>Head Coach</h3>

			<img alt="Vue logo" src="../assets/mat.jpg" />

            <div>
                Head Coach Mat Strong has a variety of experience to pull from
                in order to help you meet your goals. Mat has experience as a
                collegiate athlete, being a long-time soccer player as well
                experience in football, baseball, basketball and track and
                field. This experience is leaned on to know the demands of the
                sports that athletes & clients are performing in. Numerous years
                of sport coaching, functional fitness coaching and experience
                working with sport nutrition, sport science and strength and
                conditioning teams at University of Maryland has brought our
                Head Coach to the point of opening Agoge Strong Performance
                Training. Mat Strong hold certifications and specializes in
                Functional Fitness, Sport Performance, Speed and Power
                Development, & Olympic Weightlifting. Mat also focused his
                undergrad studies on sport psychology studying how psychological
                skills training can help develop higher levels of performance as
                well as be a preventative measure against mental illness.
            </div>
            <div>
                Credentials:B.S. Kinesiology University of
                MarylandNSCA-CSCSUSAW- Sport Performance CoachCrossFit
                Level-1NASE-CSS Level II NSPA-CCSUS Soccer- E LiscenseCurrently
                Studying for M.S. in Human Performance and Injury Prevention
            </div>
        </ul>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Navigation from '@/components/Navigation.vue'; // @ is an alias to /src

@Options({
    components: {
        Navigation
    }
})
export default class About extends Vue {}
</script>

<style lang="scss" scoped>
.background-container {
    background-color: rgba(0, 0, 0, 0.5);
}
</style>
