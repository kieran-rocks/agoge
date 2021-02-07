<template>
    <div class="main-logo">
        <img class="image" src="../assets/full_logo.png" />
    </div>

    <div class="action">
        <div class="call-button-container">
            <img
                @click="routeToProgram('fitness')"
                class="image"
                src="../assets/button_fitness.png"
            />

            <img
                @click="routeToProgram('sport')"
                class="image"
                src="../assets/button_sport.png"
            />
        </div>
    </div>
</template>

<style lang="scss">
.main-logo {
    height: 10rem;

    img {
        height: 100%;
        margin: 2rem 0 0 1.5rem;
    }
}

.action {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;

    .call-button-container {
        height: 25%;

        .image {
            height: 100%;
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
