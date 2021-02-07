<template>
    <img class="background-image" src="./assets/gym_photos/gym5_bw.jpg" />
    <router-view />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
@Options({
    components: {
        HelloWorld
    }
})
export default class Home extends Vue {}
</script>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: white;
    height: 100vh;

    nav {
        position: absolute;
        top: 0;
    }

    .background-image {
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: auto;
        filter: brightness(50%);
        z-index: -1;
    }

    /* Rules for sizing the icon. */
    .material-icons.md-18 {
        font-size: 18px;
    }
    .material-icons.md-24 {
        font-size: 24px;
    }
    .material-icons.md-36 {
        font-size: 36px;
    }
    .material-icons.md-180 {
        font-size: 180px;
    }

    /* Rules for using icons as black on a light background. */
    .material-icons.md-dark {
        color: rgba(0, 0, 0, 0.54);
    }
    .material-icons.md-dark.md-inactive {
        color: rgba(0, 0, 0, 0.26);
    }

    /* Rules for using icons as white on a dark background. */
    .material-icons.md-light {
        color: rgba(255, 255, 255, 1);
    }
    .material-icons.md-light.md-inactive {
        color: rgba(255, 255, 255, 0.3);
    }
}

#nav {
    padding: 30px;
}
</style>
