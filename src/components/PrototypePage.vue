<template>
    <!--  Prototype Page  -->
    <div id="prototype-page" @scroll="scrollContent()">
        <table>
            <transition name="slide-fade">
                <!--            <tr id="FromInsightToIdeas" v-if="show.current<1" >-->
                <tr id="RapidDesignAndIteration"
                    :style="{
                backgroundImage: `url(${background.bubble})`,
             'background-repeat': 'no-repeat', 'background-size': 'cover'
            }">
                    <td class="align-middle justify-content-center">
                        <div class="row mb-2">
                            <TealTitle class="col-12" title="Prototyping"></TealTitle>
                        </div>
                        <div class="row">
                            <MainTitle class="col-12" :title="titles.title1"></MainTitle>
                        </div>
                        <div class="row text-justify my-5">
                            <Paragraph class="col-10" :content="paragraphs.content1"></Paragraph>
                        </div>
                        <div class="row justify-content-center">
                            <div class="col-12">
                                <img :src="images.image1" class="img-responsive" alt="Agile Design summer timeline">
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

                <td class="align-middle" :style="{
                'background-color': '#FFF8EE', 'background-size': 'cover'
            }">
                    <div class="row mb-2">
                        <TealTitle class="col-12"
                                   title="What were the methods we used?"></TealTitle>
                    </div>
                    <div class="row">
                        <MainTitle class="col-12" :title="titles.title2"></MainTitle>
                    </div>
                    <div class="row my-3">
                        <Paragraph class="col-11" :content="paragraphs.content2"></Paragraph>
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
                    </div>
<!--                    <HyperLink :link="link.medium1" linkname="Read the Medium Article"></HyperLink>-->
                </td>
            </tr>

            <tr id="IndividualIdeas"
                :style="{
                backgroundImage: `url(${background.wavetop})`,
             'background-repeat': 'no-repeat', 'background-size': 'cover'
            }">
                <td>
                    <div class="row mb-2">
                        <TealTitle class="col-12" title="#001 Create crafts"></TealTitle>
                    </div>
                    <div class="row">
                        <MainTitle class="col-12" :title="titles.title3"></MainTitle>
                    </div>
                    <div class="row my-5">
                        <div class="col-12">
                            <Paragraph class="" :content="paragraphs.content3"></Paragraph>
                        </div>
                    </div>
                    <div class="row justify-content-center">
                        <div class="col-12">
                            <img :src="images.image2" class="img-responsive" alt="User Stories, Flow and Lo-fi">
                        </div>
                    </div>
                    <div class="row my-5">
                        <div class="col-4" align="center">
                            <h7>User Stories</h7>
                        </div>
                        <div class="col-4" align="center">
                            <h7>User Flow</h7>
                        </div>
                        <div class="col-4" align="center">
                            <h7>Lofi Prototype of Challenge Mode</h7>
                        </div>
                    </div>
                </td>
            </tr>

            <tr id="WholeAppDesign"
                :style="{
                backgroundImage: `url(${background.wavebot})`,
             'background-repeat': 'no-repeat', 'background-size': 'cover'
                }">
                <td>
                    <div class="row my-2">
                        <TealTitle class="col-12" title="#002 Build the system"></TealTitle>
                    </div>
                    <div class="row">
                        <MainTitle class="col-12" :title="titles.title4"></MainTitle>
                    </div>
                    <div class="row my-5">
                        <div class="col-12">
                            <Paragraph class="" :content="paragraphs.content4"></Paragraph>
                            <div class="row justify-content-center my-5">
                                <div class="col-12">
                                    <img :src="images.image3" class="img-responsive" alt="Information Architecture, Adaptivity model and navigation">
                                </div>
                            </div>

                            <div class="row">
                                <div class="col-4" align="center">
                                    <h7>Information Architecture</h7>
                                </div>
                                <div class="col-4" align="center">
                                    <h7>Adaptivity Model</h7>
                                </div>
                                <div class="col-4" align="center">
                                    <h7>Whole App Navigation Design</h7>
                                </div>
                            </div>

                        </div>
                    </div>
                </td>
            </tr>

            <tr id="IdeaPitch"
                :style="{
                backgroundImage: `url(${background.bubble2})`,
             'background-repeat': 'no-repeat', 'background-size': 'cover'
            }">
                <td>
                    <div class="row my-2">
                        <TealTitle class="col-12" title="#003 Idea Pitch"></TealTitle>
                    </div>
                    <div class="row">
                        <MainTitle class="col-12" :title="titles.title5"></MainTitle>
                    </div>
                    <div class="row my-5">
                        <div class="col-12">
                            <Paragraph class="" :content="paragraphs.content5"></Paragraph>
                        </div>
                    </div>
                    <div class="row justify-content-center my-5">
                        <div class="col-12">
                            <img :src="images.image4" class="img-responsive" alt="Content Design">
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-4" align="center">
                            <h7>Content Design Test</h7>
                        </div>
                        <div class="col-4" align="center">
                            <h7>Design System</h7>
                        </div>
                        <div class="col-4" align="center">
                            <h7>Whole App Final Design</h7>
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
    // import HyperLink from "@/components/HyperLink";
    import Card from "@/components/Card";

    import pic1 from "@/components/images/timeline_design.png"
    import pic2 from "@/components/images/prototyping1.png"
    import pic3 from "@/components/images/prototyping2.png"
    import pic4 from "@/components/images/prototyping3.png"


    import bg1 from "@/components/images/prototype_bg1.png"
    import bg2 from "@/components/images/prototype_bg2.png"
    import bg3 from "@/components/images/prototype_bg3.png"
    import bg4 from "@/components/images/prototype_bg4.png"

    export default {
        name: "PrototypePage",
        components: {
            Paragraph,
            TealTitle,
            MainTitle,
            // HyperLink,
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
                    title1: "Rapid design and iteration in summer",
                    title2: "Prototyping overview",
                    title3: "Prototyping 1: individual ideas",
                    title4: "Prototyping 2: Whole app design",
                    title5: "Prototyping 3: Hi-fi prototype",
                },
                paragraphs: {
                    content1: "In 12 weeks in summer, we used the agile product management method to keep the prototyping and iterating process fast and flexible."
                    ,
                    content2: "In the design phase, we tried to work collaboratively by working on different components in a parallel manner."
                    ,
                    content3: "In the beginning, we started from user stories and user flows to make sure that the UI align with user needs. We prototyped for individual features in the final product."
                    ,
                    content4: "After 2-4 round iteration of each features, we needed to integrate the features together in the one system. We consolidated the information architecture and the adaptivity model(learning data flow)."
                    ,
                    content5: "At the final stage, we added the real content in the design. We tested the wording in nudge notifications. Also, we constructed a design system to help us design collaboratively."
                },
                images: {
                    image1: pic1,
                    image2: pic2,
                    image3: pic3,
                    image4: pic4
                },
                background: {
                    wavetop: bg2,
                    wavebot: bg3,
                    bubble: bg1,
                    bubble2: bg4
                },
                cards: {
                    card1: {
                        quant: "16",
                        card_title: "Prototypes",
                        card_content: "We prototyped for both the single features and the whole app. For each prototype file, we had 2 to 4 versions of prototyping to ensure that all of the prototypes are consolidated.",
                    },
                    card2: {
                        quant: "60+",
                        card_title: "Think Aloud",
                        card_content: "To test the usability of our design, we set a series of tasks to see if the users achieve the goal using the prototype. We asked the participants to think aloud to learn where we can improve."
                    },
                    card3: {
                        quant: "5",
                        card_title: "System Usability Survey (SUS)",
                        card_content: "The SUS is reliable tool for measuring the usability, consisting of 10 questions with five response range from Strongly agree to Strongly disagree. We conducted it to several participants to get a quantitative evaluation of the design."
                    },
                    card4: {
                        quant: "1",
                        card_title: "Design System",
                        card_content: "To keep the consistency of design and support the future steps, we constructed a design system and updated it with our final Hi-fi prototype."
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


    img.background {
        width: 100%;
        height: 200px;
        object-fit: fill;
    }

</style>