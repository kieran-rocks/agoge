<template>
    <div id="navigation">
        <ul>
            <img alt="Agoge" src="../assets/logos/low-res/logo_reduced.png" />
            <router-link to="/about">About</router-link>
            <router-link to="/programs">Programs</router-link>
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
    background: peru;
    padding-top: 20px;
    margin: 5px 5px 50px 5px;
    border-radius: 10px;
    padding-bottom: 10px;
    ul {
        display: flex;
        list-style: none;
        padding: 0;
        margin: 0 20px 0 0;
        img {
            width: 4rem;
            margin-top: -0.5rem;
        }
        a {
            color: rgb(178, 34, 34);
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
