<template>
    <!--  Overview Page  -->
    <!--    <div id="overview-page" @scroll="scrollContent()">-->
    <table>
        <transition name="slide-fade">
            <!--            <tr id="FromInsightToIdeas" v-if="show.current<1" >-->
            <tr>
                <td class="align-middle justify-content-center" :style="{
                'background-color': '#ECF2F8', 'background-size': 'cover'
            }">
<!--                <td class="align-middle justify-content-center">-->
                    <div class="row">
                        <TealTitle class="col-12" title="What is MindEdge Learning app"></TealTitle>
                    </div>
                    <div class="row">
                        <MainTitle class="col-12" :title="titles.title1"></MainTitle>
                    </div>
                    <div class="row text-justify">
                        <Paragraph class="col" :content="paragraphs.content1"></Paragraph>
                    </div>
                    <div class="row justify-content-center">
                        <div class="col-12">
                            <img :src="images.image1" class="img-responsive" alt="MindEdge App Hifi Prototype">
                        </div>
                    </div>
                </td>

            </tr>

        </transition>

            <tr>
                <td class="align-middle justify-content-center">
                    <!--                <td class="align-middle justify-content-center">-->

                    <div class="row">
                        <MainTitle class="col-12" :title="titles.title2"></MainTitle>
                    </div>
                    <div class="row text-justify">
                        <Paragraph class="col" :content="paragraphs.content2"></Paragraph>
                    </div>
                    <div class="row">
                        <div class="col-4">
                            <img :src="images.image2" class="img-responsive" alt="METALS logo">
                        </div>
                        <div class="col-8">
                            <Paragraph class="col" :content="paragraphs.content3"></Paragraph>
                        </div>
                    </div>
                    <div class="row justify-content-center">
                        <div class="col-4">
                            <img :src="images.image3" class="img-responsive" alt="MindEdge logo">
                        </div>
                        <div class="col-8">
                            <Paragraph class="col" :content="paragraphs.content4"></Paragraph>
                        </div>
                    </div>
                </td>

            </tr>



    </table>
    
</template>

<script>

    import TealTitle from "@/components/TealTitle";
    import MainTitle from "@/components/MainTitle";
    import Paragraph from "@/components/Paragraph";

    import pic1 from "@/components/images/banner.png"
    import pic2 from "@/components/images/metals.png"
    import pic3 from "@/components/images/me_logo.png"
    // import pic4 from "@/components/images/stickynotes.png"
    // import pic5 from "@/components/images/speeddating.png"
    // import pic6 from "@/components/images/pitcheval.png"

    import background_wave_bubbles from "@/components/images/overview-bg.png"
    // import background_wave_bot from "@/components/images/wavebot.png"
    // import background_bubble from "@/components/images/bubblebackground.png"
    // import background_wave from "@/components/images/wavebackground.png"

    export default {
        name: "OverviewPage",
        components: {
            Paragraph,
            TealTitle,
            MainTitle
        },
        mounted() {
            document.addEventListener('wheel', this.scrollContent);
        },
        data: function () {
            return {
                show: {
                    // TODO may need to lift these numbers to upper layer, i.e. App.vue
                    current: 0,
                    prev: -1
                },
                titles: {
                    title1: "MindEdge learning app, making adult learning portable and flexible",
                    title2: "About the Project",
                    title3: "5 key features"
                },
                paragraphs: {
                    content1: "MindEdge Learning is a mobile app that helps Community College students and other adult learners achieve the learning success."
                    ,
                    content2: "This project is CMU METALS’s 2020 capstone project. It is a seven-month project collaboratively completed by MindEdge team and the students team."
                    ,
                    content3: "METALS (Masters of Educational Technology and Applied Learning Science) is a one-year, interdisciplinary Master's program at Carnegie Mellon University’s Human-Computer Interaction Institute, which trains students to apply evidence-based learning principles and utilize a user-centered design methodology to create engaging and effective educational products."
                    ,
                    content4: "MindEdge Learning is on a mission to improve the way the world learns. MindEdge has developed comprehensive, digital-first courseware built with adult learners in mind. MindEdge has For Credit, Professional Development, Continuing Education and Custom Solutions products."
                    ,
                    content5: "MindEdge app consists of five primary features: Chunked Modules, On-the-go challenge mode, Trophies, Nudge, and Scaffolded hint. Each of these features plays a role in helping users learn efficiently to achieve their learning goal and save time for their work or family."
                },
                images: {
                    image1: pic1,
                    image2: pic2,
                    image3: pic3
                    // image4: pic4,
                    // image5: pic5,
                    // image6: pic6
                },
                background: {
                    wavebubbles: background_wave_bubbles,
                    // wevebot: background_wave_bot,
                    // bubble: background_bubble,
                    // wave: background_wave
                }
            }
        },
        methods: {
            scrollContent: function (event) {
                if (event.deltaY > 0) {
                    this.show.prev = this.show.current;
                    this.show.current++;
                }
                if (event.deltaY < 0) {
                    this.show.prev = this.show.current;
                    this.show.current--;
                }

                console.log(this.show.current);
            }
        },
        destroy() {
            document.removeEventListener('wheel');
        }
    }
</script>

<style scoped>
    .img-responsive {
        width: 100%;
    }

    .backgroundTop {
        align-items: flex-start;
        /*display: flex;*/
    }

    .backgroundF9F8FF {
        background-color: #F9F8FF;
    }

    /*#backgroundWaveTop{*/
    /*    position: sticky;*/
    /*    top: 2rem;*/
    /*}*/

    img.background {
        width: 100%;
        height: 200px;
        object-fit: fill;
    }


    /*TODO slide*/
    .slide-enter-active {
    }

    .slide-leave-active {
    }

    .slide-leave-to {
    }

    .slide-enter {
    }

    /*TODO adjust slide animation*/
    /* Enter and leave animations can use different */
    /* durations and timing functions.              */
    .slide-fade-enter-active {
        transition: all .5s ease-in-out;
        transition-delay: .5s;
        /*transition: all .3s ease;*/
    }

    .slide-fade-leave-active {
        /*transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);*/
        transition: all .5s ease-in;

    }

    .slide-fade-leave-to
        /* .slide-fade-leave-active below version 2.1.8 */
    {
        transform: translateY(-100vh);
        /*opacity: 0;*/
    }

    .slide-fade-enter {
        transform: translateY(90vh);
        /*opacity: 0;*/
    }

</style>