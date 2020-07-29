<template>
    <h5>{{title}}</h5>
</template>

<script>
    export default {
        name: "TealTitle",
        props: {
            title: String
        }
    }
</script>

<style scoped>
    h5 {
        font-family: Lato, sans-serif;
        font-style: normal;
        font-weight: bold;
        font-size: 18px;
        line-height: 22px;

        color: #0081B8;
    }
</style>