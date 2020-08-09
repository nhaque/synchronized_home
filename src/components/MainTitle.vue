<template>
    <h1>{{title}}</h1>
</template>

<script>
    export default {
        name: "MainTitle",
        props:{
            title: String
        }
    }
</script>

<style scoped>
    h1{
        font-family: Libre Baskerville,serif;
        font-style: normal;
        font-weight: bold;
        font-size: 28px;
        line-height: 140%;
        /* or 39px */

        color: #222222;
    }
</style>