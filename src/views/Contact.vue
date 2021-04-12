<template>
    <div id="nav">
        <Navigation />
    </div>

    <div class="program-info">
        <div class="background-container">
            <div class="bullet"><b>Call me bruh: </b> (301)848-5949</div>

            <div class="bullet">
                <b>Follow me bruh: </b> @agoge.strong.performance
            </div>
        </div>
    </div>
</template>

<style lang="scss">
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
    components: {
        Navigation
    }
})
export default class Contact extends Vue {}
</script>
