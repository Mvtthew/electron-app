<template>
    <div id="app">
        <navbar></navbar>
        <router-view/>
    </div>
</template>

<style lang="scss">
    :not(input):not(textarea),
    :not(input):not(textarea)::after,
    :not(input):not(textarea)::before {
        -webkit-user-select: none;
        user-select: none;
        cursor: default;
    }
    input, button, textarea, :focus {
        outline: none; // You should add some other style for :focus to help UX/a11y
    }
</style>

<script>
    import Navbar from "./components/Navbar";
    export default {
        components: {Navbar}
    }
</script>