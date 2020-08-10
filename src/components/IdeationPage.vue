<template>
    <!--  Ideation Page  -->
    <div id="ideation-page" @scroll="scrollContent()">
        <table>
            <transition name="slide-fade">
                <!--            <tr id="FromInsightToIdeas" v-if="show.current<1" >-->
                <tr id="FromInsightToIdeas container">
                    <td class="align-middle justify-content-center">
                        <div class="row mb-3">
                            <TealTitle class="col-12" title="Ideation"></TealTitle>
                        </div>
                        <div class="row">
                            <MainTitle class="col-12" :title="titles.title1"></MainTitle>
                        </div>
                        <div class="row text-justify my-4">
                            <Paragraph class="col" :content="paragraphs.content1"></Paragraph>
                        </div>
                        <div class="row justify-content-center">
                            <div class="col-12">
                                <img id="workshop" :src="images.image1" class="img-responsive" alt="design workshop">
                            </div>
                        </div>
                    </td>

                </tr>
            </transition>

            <!--            <tr id="PossibleDesignOpp" v-if="show.current>=1" >-->
            <tr id="PossibleDesignOpp" :style="{
                backgroundImage: `url(${background.wave})`,
             'background-repeat': 'no-repeat', 'background-size': 'cover'
            }">

                        <td id="backgroundWaveTop" class="backgroundTop ">
                            <div class="row mb-3">
                                <TealTitle class="col-12"
                                           title="#001 Kick-off meeting and the design workshop"></TealTitle>
                            </div>
                            <div class="row">
                                <MainTitle class="col-12" :title="titles.title2"></MainTitle>
                            </div>
                            <div class="row my-5">
                                <Paragraph class="col-8 my-auto" :content="paragraphs.content2"></Paragraph>
                                <div class="col-4">
                                    <img :src="images.image2" class="align-middle" alt="kickoff meeting">
                                </div>
                            </div>
                            <HyperLink :link="link.medium1" linkname="Read the Medium Article"></HyperLink>
                        </td>
            </tr>

            <tr>
                <td class="backgroundF9F8FF">
                    <div class="row mb-3">
                        <div class="col">
                    <TealTitle :title="titles.tealtitle1"></TealTitle>
                        </div>
                    </div>
                    <div class="row mb-3">
                        <div class="col">
                    <MainTitle :title="titles.title3"></MainTitle>
                        </div>
                    </div>
                    <div class="row my-3">
                        <div class="col">
                    <Paragraph :content="paragraphs.content3"></Paragraph>
                        </div>
                    </div>
                    <div class="row my-3">
                    <div class="col">
                    <HyperLink :link="link.medium2" linkname="Read the Medium Article"></HyperLink>
                    </div>
                    </div>
                    <div class="row justify-content-center my-5">
                        <div class="col-xl-3 col-lg-6 col-sm-12">
                            <Card :quant="cards.card1.quant" :card_title="cards.card1.card_title"
                                  :card_content="cards.card1.card_content"></Card>
                        </div>
                        <div class="col-xl-3 col-lg-6 col-sm-12">
                            <Card :quant="cards.card2.quant" :card_title="cards.card2.card_title"
                                  :card_content="cards.card2.card_content"></Card>
                        </div>
                        <div class="col-xl-3 col-lg-6 col-sm-12">
                            <Card :quant="cards.card3.quant" :card_title="cards.card3.card_title"
                                  :card_content="cards.card3.card_content"></Card>
                        </div>
                        <div class="col-xl-3 col-lg-6 col-sm-12">
                            <Card :quant="cards.card4.quant" :card_title="cards.card4.card_title"
                                  :card_content="cards.card4.card_content"></Card>
                        </div>
                    </div>

                </td>
            </tr>

            <tr id="OnlineCollaboration"
                :style="{
                backgroundImage: `url(${background.bg4})`,
             'background-repeat': 'no-repeat', 'background-size': 'cover'
            }">
                        <td>
                            <div class="row mb-3">
                                <TealTitle class="col-12" title="Online working session"></TealTitle>
                            </div>
                            <div class="row">
                                <MainTitle class="col-12" :title="titles.title4"></MainTitle>
                            </div>
                            <div class="row">
                                <div class="col-6 my-auto mr-5">
                                    <Paragraph class="" :content="paragraphs.content4"></Paragraph>
                                </div>
                                <div class="col-4">
                                    <img :src="images.image3" class="align-middle" alt="miro collab">
                                </div>
                            </div>

                            <div class="row">
                                <div class="col">
                                    <HyperLink class="" :link="link.medium3"
                                               linkname="Read the Medium Article"></HyperLink>
                                </div>
                            </div>
                            <div class="row my-5">
                                    <img :src="images.image4" class="align-middle" alt="sticky notes">
                            </div>
                        </td>
            </tr>

            <tr id="SelectingFeatures"
                :style="{
                backgroundImage: `url(${background.bubble})`,
             'background-repeat': 'no-repeat',  'background-size': 'cover'
            }">
                <td>
                    <div class="row mb-3">
                        <TealTitle class="col-12" title="#003 Idea pitch"></TealTitle>
                    </div>
                    <div class="row">
                        <MainTitle class="col-12" :title="titles.title5"></MainTitle>
                    </div>
                    <div class="row my-5">
                        <div class="col-10">
                            <Paragraph class="" :content="paragraphs.content5"></Paragraph>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-6" align="center"><img :src="images.image5" class="row mb-3" alt="sticky notes miro">
                            <h7>Idea Pitch</h7>
                        </div>
                        <div class="col-6" align="center"><img :src="images.image6" class="row mb-3 align-middle" alt="miro collab">
                            <h7>Quantitative Evaluation</h7>
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
    import HyperLink from "@/components/HyperLink";
    import Card from "@/components/Card";

    import pic1 from "@/components/images/ideation1.png"
    import pic2 from "@/components/images/kickoff.png"
    import pic3 from "@/components/images/miro.png"
    import pic4 from "@/components/images/stickynotes.png"
    import pic5 from "@/components/images/speeddating.png"
    import pic6 from "@/components/images/pitcheval.png"

    import background_wave_top from "@/components/images/wavetop.png"
    import background_wave_bot from "@/components/images/wavebot.png"
    import background_bubble from "@/components/images/ideation-bg5.png"
    import background_wave from "@/components/images/wavebackground.png"
    import bg4 from "@/components/images/Ideation-bg4.png"

    export default {
        name: "IdeationPage",
        components: {
            Paragraph,
            TealTitle,
            MainTitle,
            HyperLink,
            Card
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
                    title1: "From insights to ideas: design workshop and idea evaluation",
                    title2: "What are the possible design opportunities?",
                    title3: "From Research insights to ideas",
                    title4: "Remote online collaboration",
                    title5: "Downselected the featured ideas",
                    tealtitle1: "#002 Internal ideation section",
                },
                paragraphs: {
                    content1: "In the Ideation phase, we wanted to brainstorm as many idea as possible and captured the best ideas. We conducted one design workshop with clients involved, several internal brainstorming sessions and three round of idea pitch meeting which invited different stakeholders."
                    ,
                    content2: "In the kick-off meeting, to share the understanding of the context, the goal, and the design opportunities among our clients and the team members, we invited all of the participants join in a design workshop. In the 2-hour session, we communicated about the desired business, product and experience states, empathized the potential users and learned about the typical user journey."
                    ,
                    content3: "After learning about the users and their pain points in the research phase, we started to ideate the possible solutions. Below are the methods we us in the internal ideation section:"
                    ,
                    content4: "In the special period of time, we had to conduct all the interal working session online. So we used Miro and Zoom to share ideas and discuss. We wrote down these rules on virtual sticky notes and pin them onto the board"
                    ,
                    content5: "We conducted several idea pitch in Zoom to get the feedbacks to the ideas we selected. In the 3-hour idea pitch, we presented ideas and ask the participants to evaluate the ideas by feasibility, impact and desirability."
                },
                images: {
                    image1: pic1,
                    image2: pic2,
                    image3: pic3,
                    image4: pic4,
                    image5: pic5,
                    image6: pic6
                },
                background: {
                    wavetop: background_wave_top,
                    wevebot: background_wave_bot,
                    bubble: background_bubble,
                    wave: background_wave,
                    bg4: bg4
                },
                link: {
                    medium1: "https://medium.com/metals-capstone-2020-syncronized/client-kick-off-defining-the-scope-of-the-project-9914ab4952b",
                    medium2: "https://medium.com/metals-capstone-2020-syncronized/our-research-scope-and-methods-d41fe09538c2",
                    medium3: "https://medium.com/metals-capstone-2020-syncronized/online-design-research-what-and-how-efb90d7a82cf"
                },
                cards: {
                    card1: {
                        quant: "28",
                        card_title: "How Might We(HMW) Questions",
                        card_content: "“How Might We” is a brainstorming technique that turns challenges into opportunities for design. We summarized the final problem space using HMW, which can be categorized into 5 areas.",
                    },
                    card2: {
                        quant: "300+",
                        card_title: "Brainstorming ideas",
                        card_content: "In the brainstorming session, our goal is to get as many ideas as possible. We set limited time and target number of ideas covering all the HMW questions."
                    },
                    card3: {
                        quant: "21",
                        card_title: "Storyboards",
                        card_content: "For each idea we selected, we drew a storyboard with 3 specific components: \n" +
                            "(i) What problem will the idea solve?\n" +
                            "(ii) How does the idea work?\n" +
                            "(iii) The good impact of the idea."
                    },
                    card4: {
                        quant: "3",
                        card_title: "Speed-dating session",
                        card_content: "Speed dating is a user research method to test multiple ideas quickly with the intended users or stakeholders in a short time to figure out what are their real needs and concerns. This method is a good way to find out the future design direction."
                    }
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

    #workshop {
        width: 100%;
        height: auto;
        filter: drop-shadow(0px 0px 15px rgba(0, 0, 0, 0.25));
        border-radius: 10px;
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