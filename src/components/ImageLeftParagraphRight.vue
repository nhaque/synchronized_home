<template>
    <div class="row">
        <div class="col-2"><img :src="image_src"></div>
        <div class="col-10">
            <div class="row">
                <h5>{{title}}</h5>
            </div>
            <div class="row">
                <Paragraph :content="paragraph_content"></Paragraph>
            </div>
        </div>
    </div>
</template>

<script>
    import Paragraph from "@/components/Paragraph";

    export default {
        name: "ImageLeftParagraphRight",
        components: {Paragraph},
        props:{
            image_src: String,
            paragraph_content: String,
            title: String
        }
    }
</script>

<style scoped>

    h5{
        font-family: Lato, sans-serif;
        font-style: normal;
        font-weight: bold;
        font-size: 20px;
        line-height: 24px;
        display: flex;
        align-items: center;

        color: #222222;
    }

</style>