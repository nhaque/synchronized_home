<template>
    <!--  Overview Page  -->
    <!--    <div id="overview-page" @scroll="scrollContent()">-->
    <table>
        <transition name="slide-fade">
            <!--            <tr id="FromInsightToIdeas" v-if="show.current<1" >-->
            <tr id="app-intro">
                <td class="align-middle justify-content-center" :style="{
                'background-color': '#ECF2F8', 'background-size': 'cover'
            }">
                    <!--                <td class="align-middle justify-content-center">-->
                    <div class="row mt-6">
                        <TealTitle class="col-12" title="What is MindEdge Learning app"></TealTitle>
                    </div>
                    <div class="row mb-3">
                        <MainTitle class="col-12" :title="titles.title1"></MainTitle>
                    </div>
                    <div class="row text-justify mb-3">
                        <Paragraph class="col" :content="paragraphs.content1"></Paragraph>
                    </div>
                    <div class="row">
                            <img :src="images.image1" class="img-responsive col" alt="MindEdge App Hifi Prototype">
                    </div>
                    <div class="row my-7">
                           <button id="demo_btn" class="btn btn-primary offset-5 col-2">
                              Request Demo
                           </button>
                    </div>

                </td>

            </tr>

        </transition>

        <tr>
            <td class="align-middle justify-content-center">
                <!--                <td class="align-middle justify-content-center">-->

                <div class="row mb-3">
                    <MainTitle class="col-12" :title="titles.title2"></MainTitle>
                </div>
                <div class="row text-justify">
                    <Paragraph class="col" :content="paragraphs.content2"></Paragraph>
                </div>
                <div class="row justify-content-center my-5">
                    <div class="col-4">
                        <img :src="images.image2" class="img-responsive" alt="METALS logo">
                    </div>
                    <div class="col-8">
                        <Paragraph class="col" :content="paragraphs.content3"></Paragraph>
                    </div>
                </div>
                <div class="row justify-content-center">
                    <div class="col-4">
                        <img :src="images.image3" class="img-responsive" alt="Failed to display image">
                    </div>
                    <div class="col-8">
                        <Paragraph class="col" :content="paragraphs.content4"></Paragraph>
                    </div>
                </div>
            </td>

        </tr>

        <tr id="persona">
            <td class="align-middle justify-content-center">
                <div class="row mb-2">
                    <TealTitle class="col-12" :title="titles.title3"></TealTitle>
                </div>
                <div class="row mb-5">
                    <MainTitle class="col-12" :title="titles.title4"></MainTitle>
                </div>
                <div class="row justify-content-center">
                    <div class="col-12">
                        <img id="persona-img" :src="images.persona">
                    </div>
                </div>
            </td>

        </tr>

        <tr id="problem-space">
            <td class="align-middle justify-content-center">
                <div class="row justify-content-center mb-2">
                    <TealTitle class="col-12" :title="titles.title5"></TealTitle>
                </div>
                <div class="row justify-content-center">
                    <p id="hmw" class="col-12 my-3">
                        How Might We design a mobile learning experience that is
                        <span id="engaging">engaging</span>, <span id="easy">easy to use</span> and
                        <span id="supportive"> supportive </span> to help with career and academic success?
                    </p>
                </div>
            </td>

        </tr>


        <tr id="feature-introduction"
            :style="{
                backgroundImage: `url(${background.wavebubbles})`,
             'background-repeat': 'no-repeat', 'background-size': '100% 100%'
            }">
            <td class="align-middle justify-content-center">
                <div class="row justify-content-center mb-2">
                    <TealTitle class="col-12" title="Our Solution"></TealTitle>
                </div>
                <div class="row">
                    <MainTitle class="col-12" :title="titles.title6"></MainTitle>
                </div>

                <div class="row mb-7">
                    <Paragraph class="col-12" :content="paragraphs.key_feature"></Paragraph>
                </div>

                <div class="row my-5">
                    <div class= "col-7 my-auto mr-6">
                        <div class="row mb-2">
                            <h3 class="col">Chunked Modules</h3>
                        </div>
                        <div class="row">
                        <Paragraph class="col-12" :content="paragraphs.chunked_module"></Paragraph>
                        </div>
                    </div>
                    <div class="col-3 ml-5">
                        <img :src="images.chunked_module" class="align-middle">
                    </div>
                </div>

                <div class="row my-5">
                    <div class="col-3 mr-5">
                        <img :src="images.on_the_go" class="align-middle">
                    </div>
                    <div class= "col-7 my-auto mr-6">
                        <div class="row mb-2">
                            <h3 class="col">On-the-go challenge mode</h3>
                        </div>
                        <div class="row">
                            <Paragraph class="col-12" :content="paragraphs.on_the_go"></Paragraph>
                        </div>
                    </div>
                </div>

                <div class="row my-5">
                    <div class="col-7 my-auto mr-6">
                        <div class="row mb-2">
                            <h3 class="col">Trophies</h3>
                        </div>
                        <div class="row">
                            <Paragraph class="col-12" :content="paragraphs.trophies"></Paragraph>
                        </div>
                    </div>
                    <div class="col-3 ml-5">
                        <img :src="images.trophies" class="align-middle">
                    </div>
                </div>

                <div class="row my-5">
                    <div class="col-3 mr-5">
                        <img :src="images.nudge" class="align-middle">
                    </div>
                    <div class="col-7 my-auto  mr-6">
                        <div class="row mb-2">
                            <h3 class="col">Nudge</h3>
                        </div>
                        <div class="row">
                            <Paragraph class="col-12" :content="paragraphs.nudge"></Paragraph>
                        </div>
                    </div>
                </div>

                <div class="row my-5">
                    <div class="col-7 my-auto mr-6">
                        <div class="row mb-2">
                            <h3 class="col">Scaffolded Hint</h3>
                        </div>
                        <div class="row">
                            <Paragraph class="col-12" :content="paragraphs.scaffold_hint"></Paragraph>
                        </div>
                    </div>
                    <div class="col-3 ml-5">
                        <img :src="images.scaffold_hint" class="align-middle">
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

    import pic1 from "@/components/images/app_intro.png"
    import pic2 from "@/components/images/metals.png"
    import pic3 from "@/components/images/me_logo.png"

    import chunked_module from "@/components/images/chunking.gif"
    import nudge from "@/components/images/nudge.gif"
    import on_the_go from "@/components/images/challenge.gif"
    import scaffold_hint from "@/components/images/scaffold_hint.gif"
    import trophies from "@/components/images/trophies.gif"


    import background_wave_bubbles from "@/components/images/overview-bg.png"


    import persona from "@/components/images/overview-persona.png"


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
                    title3: "Who are we designing for?",
                    title4: "Non-traditional students enrolled in online community colleges",
                    title5: "The Problem Space",
                    title6: "5 key features"
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
                    ,
                    hmw: "How Might We design a mobile learning experience that is engaging, easy to use and supportive to help with career and academic success?"
                    ,
                    key_feature: "MindEdge app consists of five primary features: Chunked Modules, On-the-go challenge mode, Trophies, Nudge, and Scaffolded hint. Each of these features plays a role in helping users learn efficiently to achieve their learning goal and save time for their work or family."
                    ,
                    chunked_module: "MindEdge Learning chunks content into smaller units based on what type of content it is. Each chunk of content is placed in one card. The progress bar on the top indicates students’ current progress in this module. Students move on to the next card by swiping or clicking on the “continue” button at the bottom."
                    ,
                    on_the_go: "MindEdge provides students with an adaptive learning experience by offering them the opportunities to practice skills they haven’t mastered yet quickly. Students can review the results from last time’s practice, see the detailed explanations, and are encouraged to revisit the module they are struggling with."
                    ,
                    trophies: "We designed app-level trophies to encourage retention and learner motivation and course-level trophies to encourage content engagement."
                    ,
                    nudge: "Based on the learning science theory, we added nudge in our system to help learners improve their self-regulation skill."
                    ,
                    scaffold_hint: "We added a new feature “hint” to offer students several levels of hints. Students can click on “Hint” to reveal one hint at a time.  and the hints will become more and more specific as they click through them."
                },

                images: {
                    image1: pic1,
                    image2: pic2,
                    image3: pic3,
                    persona: persona,
                    chunked_module: chunked_module,
                    nudge: nudge,
                    on_the_go: on_the_go,
                    scaffold_hint: scaffold_hint,
                    trophies: trophies
                    // image4: pic4,
                    // image5: pic5,
                    // image6: pic6
                },
                background: {
                    wavebubbles: background_wave_bubbles
                }
            }
        },
    }
</script>

<style scoped>


    img.background {
        width: 100%;
        height: 200px;
        object-fit: fill;
    }

    .mr-6,
    .mx-6 {
        margin-right: 5rem !important;
    }

    .ml-6,
    .mx-6 {
        margin-right: 5rem !important;
    }


    .mt-7,
    .my-7 {
        margin-top: 7rem !important;
    }

    .mb-7,
    .my-7 {
        margin-bottom: 7rem !important;
    }

    #app-intro {
        height: 130vh;
    }

    #persona {
        background-color: #ECF2F8;
        height: 120vh;
    }

    #problem-space {
        background-color: #FFF8EE;
        height: 50vh;
    }

    #hmw {
        font-family: Josefin Sans, Libre Baskerville, serif;
        font-style: normal;
        font-weight: bold;
        font-size: 30px;
        line-height: 120%;
        color: #111111;
    }

    #feature-introduction {
        height: 350vh;
    }

    #request_demo {
        background: #0081B8;
        box-shadow: 0px 3px 16px rgba(0, 0, 0, 0.25);
        border-radius: 10px;
    }

    #engaging {
        color: #02B1E1;
    }

    #easy {
        color: #E8A647;
    }

    #supportive {
        color: #EF4A42;
    }

    #demo_btn {
        width: 178px;
        height: 73px;
        background: #0081B8;
        box-shadow: 0px 3px 16px rgba(0, 0, 0, 0.25);
        border-radius: 10px;
        line-height: 100%;
        font-family: Lato, sans-serif;
        font-style: normal;
        font-weight: bold;
        font-size: 18px;
        text-align: center;
        color: #FFFFFF;
    }

</style>