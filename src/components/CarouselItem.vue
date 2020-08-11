<template>
    <div class="container-fluid mt-3">
        <div class="row">
            <div class="col">
                <h3>{{item_title}}</h3>
            </div>
        </div>
        <div class="row">
            <div class="col-9">
                <div class="row">
                    <div class="col-12">
                        <Paragraph :content="item_paragraph"></Paragraph>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <h4>How to implement</h4>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <PencilBullet :list_texts="pencil_bullet_array"></PencilBullet>
                    </div>
                </div>
            </div>
            <div class="col-3 align-middle my-auto">
                <img :src="img_src">
            </div>
        </div>
    </div>
</template>

<script>
    import Paragraph from "@/components/Paragraph";
    import PencilBullet from "@/components/PencilBullet";

    export default {
        name: "CarouselItem",
        components: {
            PencilBullet,
            Paragraph
        },
        props:{
            item_title: String,
            item_paragraph: String,
            pencil_bullet_array: Array,
            img_src: String
        }
    }
</script>

<style scoped>
    h4{
        font-family: Avenir;
        font-style: normal;
        font-weight: normal;
        font-size: 18px;
        line-height: 130%;
        /* or 23px */
        color: #0081B8;
    }

    carouselItem{
        height: 100%;
    }

</style>