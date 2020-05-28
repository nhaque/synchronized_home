<template>
    <ul class="pencilBulletList list-group text-left">
        <li v-for="(text, index) in list_texts" :key="index" class="list-group-item py-1 pl-3 pencilItem">&#x270D; {{text}}</li>
    </ul>
</template>

<script>
    export default {
        name: "PencilBullet",
        props: {
            list_texts: Array
        }
    }
</script>

<style scoped>
    .pencilItem{
        border-width:0;

        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: 300;
        font-size: 14px;
        line-height: 150%;
        /* or 21px */
        color: #222222;
    }
</style>