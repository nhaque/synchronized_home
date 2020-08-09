<template>
    <a :href="link">{{linkname}}</a>
</template>

<script>
    export default {
        name: "HyperLink",
        props:{
            link: String,
            linkname: String,
        }
    }
</script>

<style scoped>
    a{
        font-family: Lato, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 20px;
        line-height: 140%;
        /* identical to box height, or 28px */

        text-decoration-line: underline;

        color: #2F80ED;
    }
</style>