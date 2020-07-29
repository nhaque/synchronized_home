<template>
    <!--  Ideation Page  -->
    <div id="ideation-page" class="container">
        <table>
        <tr>
            <td class="align-middle">
        <div class="row">
            <TealTitle class="col-12" title="Ideation"></TealTitle>
        </div>
        <div class="row">
            <MainTitle class="col-12" :title="titles.title1"></MainTitle>
        </div>
        <div class="row text-justify">
            <Paragraph class="col" :content="paragraphs.content1"></Paragraph>
        </div>
        <div class="row justify-content-center">
            <div class="col-12">
                <img :src="images.image1" class="img-responsive" alt="design workshop">
            </div>
        </div>
            </td>
        </tr>
        </table>
    </div>
</template>

<script>
    import TealTitle from "@/components/TealTitle";
    import MainTitle from "@/components/MainTitle";
    import Paragraph from "@/components/Paragraph";

    import pic1 from "@/components/images/ideation1.png"

    export default {
        name: "IdeationPage",
        components: {
            Paragraph,
            TealTitle,
            MainTitle
        },
        data: function () {
            return {
                titles: {
                    title1: "From insights to ideas: design workshop and idea evalution"
                },
                paragraphs: {
                    content1: "In the Ideation phase, we wanted to brainstorm as many idea as possible and captured the best ideas. We conducted one design workshop with clients involved, several internal brainstorming sessions and three round of idea pitch meeting which invited different stakeholders."
                },
                images:{
                    image1: pic1
                }
            }
        }
    }
</script>

<style scoped>
    .img-responsive{
        width:100%;
    }
    tr{
        height: 100vh;
    }
</style>