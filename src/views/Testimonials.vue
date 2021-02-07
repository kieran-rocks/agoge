<template>
    <div id="nav">
        <Navigation />
    </div>

    <h1>Testimonials</h1>

    <div class="background-container">
        <div>Aaron- Tactical</div>

        <div>Katie- Tactical</div>

        <div>Kenny- Speed/Sport</div>

        <div>Trevor- Speed/Sport</div>

        <div>Kirsten- Knowledge</div>

        <div>Mike- Bodybuilding/Coaching Enthusiasm</div>

        <div>Sam/Lonnie</div>

        <div>Greg/Ben</div>
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
