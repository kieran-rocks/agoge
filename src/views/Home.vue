<template>
	<div class="main-logo">
		<img class="image" src="../assets/full_logo.png" />
	</div>

    <div class="action">
        <div class="call-button-container">
            <router-link to="/programs">
                <img class="image" src="../assets/button_fit.png" />
            </router-link>

            <router-link to="/programs">
                <img class="image" src="../assets/button_strong.png" />
            </router-link>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.main-logo {
	height: 10rem;

	img {
		height: 100%;
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
        greet() {
            //router.push(...);
            // `this` inside methods points to the current active instance
            //alert('Hello ' + this.name + '!')
            // `event` is the native DOM event
            // if (event) {
            // 	alert(event.target.tagName)
            // }
        }
    }
})
export default class Home extends Vue {}
</script>
