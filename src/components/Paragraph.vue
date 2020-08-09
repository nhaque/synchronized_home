<template>
    <p class="align-middle">{{content}}</p>
</template>

<script>
    export default {
        name: "Paragraph",
        props:{
            content:String
        }
    }
</script>

<style scoped>
    p{
        font-family: Lato, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 20px;
        line-height: 140%;
        /* or 28px */


        color: #222222;
    }

</style>