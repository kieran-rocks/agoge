<template>
    <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link> |
        <router-link to="/programs">Programs</router-link> |
        <router-link to="/testimonials">Testimonials</router-link> |
        <router-link to="/contact">Contact</router-link>
    </div>
    <img class="background-image" src="./assets/download.jpeg" />
    <router-view />
</template>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    height: 100vh;

    .background-image {
        height: 100%;
        width: 100%;
        opacity: 1.2;
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

    a {
        font-weight: bold;
        color: #2c3e50;

        &.router-link-exact-active {
            color: #42b983;
        }
    }
}
</style>
