<template>
    <div class="iconText2">
        <div class="row justify-content-center mb-4">
            <img :src="imgSrc" alt=".."/>

        </div>
        <div class="row mb-3">
            <h6 class="col-12 iconText2Title">{{icon_text_title}}</h6>
        </div>
        <div class="row">
            <div class="col-12 iconText2Text ">{{icon_text_text}}</div>
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
        font-family: Lato, sans-serif;
        font-style: normal;
        font-weight: bold;
        font-size: 20px;
        line-height: 24px;
        color: #222222;
    }

    .iconText2Text {
        font-family: Lato, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 16px;
        line-height: 130%;
        /* or 21px */
        color: #111111;
    }

    div img{

    }

</style>