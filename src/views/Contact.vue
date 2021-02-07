<template>
    <div id="nav">
        <Navigation />
    </div>

    <div class="contact">
        <h1>Call me bruh</h1>
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
export default class Contact extends Vue {}
</script>
