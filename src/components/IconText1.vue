<template>
    <div class="row m-3 iconText1">
        <div class="col-4 icon">
            <img class="image" :src="imgSrc" />
        </div>
        <div class="col-8 text-left content">
            <div class="row">
                <h6 class="col iconText1Title">{{icon_text_title}}</h6>
            </div>
            <div class="row">
                <div class="col iconText1Text">{{icon_text_text}}</div>
            </div>
            <div class="row mt-2">
                <PencilBullet :list_texts="list_texts"></PencilBullet>
            </div>
        </div>
    </div>
</template>

<script>
    import PencilBullet from "@/components/PencilBullet";
    export default {
        name: "IconText1",
        components:{
            PencilBullet
        },
        props:{
            list_texts: Array,
            icon_text_title: String,
            icon_text_text: String,
            imgSrc:String,
        }
    }
</script>

<style scoped>
    .iconText1{

    }

    .image{
        max-width: 100%;
    }
    .iconText1Title{
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: bold;
        font-size: 16px;
        line-height: 20px;

        color: #02B1E1;
    }
    .iconText1Text{
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: 300;
        font-size: 14px;
        line-height: 150%;
        /* or 16px */
        color: #111111;
    }

</style>