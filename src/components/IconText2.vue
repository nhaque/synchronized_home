<template>
    <div class="row m-3 iconText2">
        <div class="row">
            <img :src="imgSrc" class="col" alt=".."/>
        </div>
        <div class="row text-left">
            <h6 class="col iconText2Title ">{{icon_text_title}}</h6>
        </div>
        <div class="row text-left">
            <div class="col iconText2Text ">{{icon_text_text}}</div>
        </div>
    </div>
</template>

<script>

    export default {
        name: "IconText1",
        components: {

        },
        props: {
            list_texts: Array,
            icon_text_title: String,
            icon_text_text: String,
            imgSrc: String,
        }
    }
</script>

<style scoped>
    .iconText2 {
        max-width: 200px;
    }

    .iconText2Title {
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: bold;
        font-size: 16px;
        line-height: 19px;

        color: #02B1E1;
    }

    .iconText2Text {
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: 300;
        font-size: 14px;
        line-height: 150%;
        /* or 16px */
        color: #111111;
    }

    div img{
        height: 180px
    }

</style>