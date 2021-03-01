<template>
    <div class="bg-color"></div>

    <div class="bg-container"></div>
    <div class="overlap">
        <router-view />
    </div>
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
    background: black;

    nav {
        position: absolute;
        top: 0;
    }

    .overlap {
        display: flex;
        flex-direction: column;
        overflow: hidden;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }

    .bg-container {
        height: 100vh;
        // background-image: url(assets/gym_photos/gym5_bw.jpg);
        background-image: url(assets/bg.png);
        background-position: center center;
        background-repeat: no-repeat;
        background-attachment: fixed;
        background-size: cover;
        //filter: brightness(50%);
        margin: -10px;
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
