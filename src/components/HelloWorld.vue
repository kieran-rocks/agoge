<template>
    <div class="p-grid test"></div>
    <h1>HELLO</h1>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Button from 'primevue/button';

@Options({
    components: {
        Button
    },
    props: {
        msg: String
    }
})
export default class HelloWorld extends Vue {
    msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
    margin: 40px 0 0;
}
ul {
    list-style-type: none;
    padding: 0;
}
li {
    display: inline-block;
    margin: 0 10px;
}
a {
    color: #42b983;
}
.test {
    width: 100%;
}
</style>
