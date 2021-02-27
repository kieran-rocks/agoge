<template>
    <div id="navigation">
        <ul>
            <img alt="Vue logo" src="../assets/logo_small.png" />
            <router-link to="/">Home</router-link>
            <router-link to="/about">About</router-link>
            <router-link to="/programs">Programs</router-link>
            <router-link to="/testimonials">Testimonials</router-link>
            <router-link to="/contact">Contact</router-link>
        </ul>
    </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#navigation {
    display: flex;
    width: 100%;
    margin-bottom: 50px;
    ul {
        display: flex;
        list-style: none;
        padding: 0;
        margin: 0 20px 0 0;
        img {
            width: 4rem;
        }
        a {
            color: white;
            font-weight: 400;
            font-size: 2rem;
            padding: 2px 10px;
            cursor: pointer;
            text-decoration: none;
        }
        .router-link-active {
            text-decoration: underline;
        }
    }
}
</style>
