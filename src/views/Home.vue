<template>
    <div class="main-logo">
        <img class="image" src="../assets/logos/low-res/logo_full.png" />
    </div>

    <div class="sign-up">
        <router-link to="/contact">Sign up now</router-link>
    </div>

    <div class="action">
        <div class="call-button-container">
            <img
                @click="routeToProgram('performance')"
                class="image"
                src="../assets/button_sport.png"
            />

            <img
                @click="routeToProgram('fitness')"
                class="image"
                src="../assets/button_fitness_shield.png"
            />
        </div>
    </div>
</template>

<style lang="scss">
.main-logo {
    padding-top: 0.5rem;
    height: 30%;
    width: 100%;

    img {
        max-height: 100%;
        max-width: 100%;
    }
}

.action {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 5rem;

    .call-button-container {
        height: 25%;

        .image {
            max-width: 30%;
            margin: 0 3rem;
        }
    }
}
</style>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
// import router from '@vue/cli-plugin-router';

@Options({
    components: {
        HelloWorld
    },
    methods: {
        routeToProgram(programName: string) {
            this.$router.push({
                name: 'Programs',
                params: { program: programName }
            });
        }
    }
})
export default class Home extends Vue {}
</script>
