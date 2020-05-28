<template>
    <div class="sectionPage">
        <div class="row sectionHeader">
            <div class="col-2 greenBlockLarge"></div>
            <div class="offset-1 col-9 justify-content-start sectionTitle">{{section_name}}</div>
        </div>
        <div class="row sectionIndex">
            <div class="offset-7 col-1 justify-content-center greenBlockSmall"></div>
            <div class="col-4" v-for="{subtitle, index} in subtitles" :key="index">{{subtitle}} {{subtitle_page_numbers}}</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "SectionPage",
        props:{
            section_name: String,
            subtitles: Array,
            subtitle_page_numbers: Array
        },
        data: function(){
            return {
                // data fields go here
                id:[1,2]
            }
        },
        computed:{
            // computed fields go here
        },
        methods:{
            // methods go here
        }
    }
</script>

<style scoped>
    .greenBlockLarge{
        background-color: #2EC4B6;
        width:100px;
        max-height: 100%;
    }
    .greenBlockSmall{
        background-color: #2EC4B6;
        max-height: 150px;
    }
</style>