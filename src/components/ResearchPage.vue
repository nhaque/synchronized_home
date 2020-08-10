<template>
    <div id="research-page">
        <table>
            <tr>
                <td class="align-middle">
                    <TealTitle title="User-centered research"></TealTitle>
                    <MainTitle :title="main_title.title1"></MainTitle>
                    <Paragraph :content="paragraph.p1"></Paragraph>
                    <div class="row justify-content-center my-5">
                        <div class="col-lg-12 col-sm-12">
                            <img class="w-100" :src="image.design_thinking">
                        </div>
                    </div>
                </td>
            </tr>
            <tr>
                <td class="align-middle" :style="{
                'background-color': '#F7FAFE', 'background-size': 'cover'
            }">
                    <TealTitle title="What is context?"></TealTitle>
                    <MainTitle :title="main_title.title2"></MainTitle>
                    <Paragraph :content="paragraph.p2"></Paragraph>
                    <div class="row justify-content-center my-5">
                        <Card class="col-md-6 col-xs-6 my-1" :quant="card.lit_review.number" :card_title="card.lit_review.title"
                              :card_content="card.lit_review.text"></Card>

                        <Card class="col-md-6 col-xs-6 my-1" :quant="card.comp_analysis.number"
                              :card_title="card.comp_analysis.title"
                              :card_content="card.comp_analysis.text"></Card>
                        <Card class="col-md-6 col-xs-6 my-1" :quant="card.elearning.number" :card_title="card.elearning.title"
                              :card_content="card.elearning.text"></Card>
                        <Card class="col-md-6 col-xs-6 my-1" :quant="card.log_data.number" :card_title="card.log_data.title"
                              :card_content="card.log_data.text"></Card>
                    </div>
                </td>
            </tr>
            <tr>
                <td class="align-middle">

                    <div id="research_carousel" ref="research_carousel" class="carousel slide row" data-wrap="false" data-interval="false">
                        <a class="carousel-control-prev col-1" href="#research_carousel" role="button" data-slide="prev" @click="carousel_prev">
                            <span class="" aria-hidden="true"><img :src="image.carousel_arrow_left"></span>
                            <span class="sr-only">Previous</span>
                        </a>
                        <div class="carousel-inner offset-1 col-8 mx-auto py-5 ">
                            <div class="carousel-item active">
                                <CarouselItem id="carouselItem1" class=" w-100" :item_title="carousel_item.c1.title" :item_paragraph="carousel_item.c1.paragraph" :pencil_bullet_array="carousel_item.c1.pencil_array"
                                              :img_src="carousel_item.c1.img_src"></CarouselItem>
                            </div>
                            <div class="carousel-item">
                                <CarouselItem id="carouselItem2" class=" w-100" :item_title="carousel_item.c2.title" :item_paragraph="carousel_item.c2.paragraph" :pencil_bullet_array="carousel_item.c2.pencil_array"
                                              :img_src="carousel_item.c2.img_src"></CarouselItem>
                            </div>
                            <div class="carousel-item">
                                <CarouselItem id="carouselItem3" class=" w-100" :item_title="carousel_item.c3.title" :item_paragraph="carousel_item.c3.paragraph" :pencil_bullet_array="carousel_item.c3.pencil_array"
                                              :img_src="carousel_item.c3.img_src"></CarouselItem>
                            </div>
                            <div class="carousel-item">
                                <CarouselItem id="carouselItem4" class=" w-100" :item_title="carousel_item.c4.title" :item_paragraph="carousel_item.c4.paragraph" :pencil_bullet_array="carousel_item.c4.pencil_array"
                                              :img_src="carousel_item.c4.img_src"></CarouselItem>
                            </div>
                        </div>
                        <a class="carousel-control-next offset-1 col-1" href="#research_carousel" role="button" data-slide="next" @click="carousel_next">
                            <span class="" aria-hidden="true"><img :src="image.carousel_arrow_right"></span>
                            <span class="sr-only">Next</span>
                        </a>
                    </div>
                    <!--                    TODO finish carousel-->
                    <div id="carousel-slide-labels" class="row mt-5 justify-content-around">
                        <div id="carousel-label-1" class="col-3 text-center font-weight-bold">01 Chunked Courses</div>
                        <div id="carousel-label-2" class="col-3 text-center">02 Interactive Micro Content</div>
                        <div id="carousel-label-3" class="col-3 text-center">03 Continued Access</div>
                        <div id="carousel-label-4" class="col-3 text-center">04 Flexible Pedagogies</div>
                    </div>

                </td>
            </tr>

            <tr>
                <td>
                    <div class="row my-3">
                        <h6>Key Insights</h6>
                    </div>
                    <div class="row justify-content-center">
                        <div class="col">
                            <IconText2 :icon_text_title="iconText.personal_commitment.title"
                                       :icon_text_text="iconText.personal_commitment.text"
                                       :img-src="iconText.personal_commitment.icon"></IconText2>
                        </div>
                        <div class="col">
                            <IconText2 :icon_text_title="iconText.course_design.title"
                                       :icon_text_text="iconText.course_design.text"
                                       :img-src="iconText.course_design.icon"></IconText2>
                        </div>
                        <div class="col">
                            <IconText2 :icon_text_title="iconText.personalization.title"
                                       :icon_text_text="iconText.personalization.text"
                                       :img-src="iconText.personalization.icon"></IconText2>
                        </div>
                    </div>
                </td>
            </tr>
            <tr :style="{
                'background-color': '#F7FAFE', 'background-size': 'cover'
            }">
                <td>
                    <div class="row">
                        <TealTitle title="Understanding the Stakeholder Landscape" class="col"></TealTitle>
                    </div>
                    <div class="row mb-3">
                        <h2 class="col">Generative Research</h2>
                    </div>
                    <div class="row">
                        <p class="col">
                            In order to better understand the stakeholders’ needs, feelings and frustrations, we conducted
                            interviews
                            and cognitive task analysis. By the end of the spring, we came up with a stakeholder map, a adult
                            online
                            learning model, 10 insights and 3 personas.
                        </p>
                    </div>
                    <div class="row justify-content-center ">
                        <Card class="col-md-6 col-xs-6 " :quant="card.cta.number" :card_title="card.cta.title"
                              :card_content="card.cta.text"></Card>

                        <Card class="col-md-6 col-xs-6" :quant="card.interviews.number"
                              :card_title="card.interviews.title"
                              :card_content="card.interviews.text"></Card>
                        <Card class="col-md-6 col-xs-6" :quant="card.affinity_diagram.number"
                              :card_title="card.affinity_diagram.title"
                              :card_content="card.affinity_diagram.text"></Card>
                    </div>

                </td>
            </tr>
            <tr>
                <td>
                    <div class="row">
                        <TealTitle title="Understanding the Stakeholders' Feeling and Needs" class="col"></TealTitle>
                    </div>
                    <div class="row">
                        <MainTitle class="col" title="Generative Research"></MainTitle>
                    </div>
                    <div class="row mt-5">
                        <div class="col d-flex flex-row justify-content-start">
                            <ul class="nav nav-tabs d-flex flex-column col-2 align-items-end" id="myTab" role="tablist">
                                <li class="nav-item my-3" role="presentation">
                                    <a class="nav-link active" id="home-tab" data-toggle="tab" href="#instructor" role="tab" aria-controls="home" aria-selected="true">Instructor</a>
                                </li>
                                <li class="nav-item my-3" role="presentation">
                                    <a class="nav-link" id="profile-tab" data-toggle="tab" href="#learners" role="tab" aria-controls="profile" aria-selected="false">Learners</a>
                                </li>
                            </ul>
                            <div class="tab-content col-8 ml-0 py-5" id="myTabContent">
                                <div class="tab-pane fade show active" id="instructor" role="tabpanel" aria-labelledby="instructors-tab">
                                    <div class="row">
                                        <ImageLeftParagraphRight class="col" :image_src="tab_content.instructor.row_1.instructor_input" :paragraph_content="tab_content.instructor.row_1.instructor_input_paragraph"
                                                                 :title="tab_content.instructor.row_1.instructor_input_title"></ImageLeftParagraphRight>
                                    </div>
                                    <div class="row">
                                        <ImageLeftParagraphRight class="col" :image_src="tab_content.instructor.row_2.realworld_challenge" :paragraph_content="tab_content.instructor.row_2.realworld_challenge_paragraph"
                                                                 :title="tab_content.instructor.row_2.realworld_challenge_title"></ImageLeftParagraphRight>
                                    </div>
                                </div>
                                <div class="tab-pane fade" id="learners" role="tabpanel" aria-labelledby="learners-tab">
                                    <div class="row">
                                        <ImageLeftParagraphRight class="col" :image_src="tab_content.learners.row_1.image" :paragraph_content="tab_content.learners.row_1.paragraph"
                                                                 :title="tab_content.learners.row_1.title"></ImageLeftParagraphRight>
                                    </div>
                                    <div class="row">
                                        <ImageLeftParagraphRight class="col" :image_src="tab_content.learners.row_2.image" :paragraph_content="tab_content.learners.row_2.paragraph"
                                                                 :title="tab_content.learners.row_2.title"></ImageLeftParagraphRight>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </td>
            </tr>
        </table>
        <Footer></Footer>
    </div>

</template>

<script>
    import $ from 'jquery';

    import Card from "@/components/Card";
    import IconText2 from "@/components/IconText2";
    import TealTitle from "@/components/TealTitle";
    import MainTitle from "@/components/MainTitle";
    import Paragraph from "@/components/Paragraph";

    //import image
    import image46 from "../assets/image46.png"
    import image47 from "../assets/image47.png"
    import image48 from "../assets/image48.png"
    import image49 from "../assets/image49.png"
    import image50 from "../assets/image50.png"
    import image51 from "../assets/image51.png"
    import image52 from "../assets/image52.png"
    import image53 from "../assets/image53.png"
    import image1 from "../assets/image1.png"
    import image2 from "../assets/image2.png"
    import image3 from "../assets/image3.png"
    import double_diamond from "../assets/double_diamond.png"
    import design_thinking from "@/components/images/design_thinking_diagram.png"
    import CarouselItem from "@/components/CarouselItem";
    import four_cube from "@/components/images/fourcube.png"
    import pointer from "@/components/images/pointer.png";
    import screens from "@/components/images/screens.png";
    import toss_up from "@/components/images/toss_up.png"
    import carousel_arrow_right from "@/components/images/carousel_arrow_right.png"
    import carousel_arrow_left from "@/components/images/carousel_arrow_left.png"
    import ImageLeftParagraphRight from "@/components/ImageLeftParagraphRight";
    import instructor_input from "@/components/images/instructor_input.png";
    import realworld_challenge from "@/components/images/realworldchallenge.png"
    import long_term from "@/components/images/learnterm.png"
    import flexibility from "@/components/images/flexibility.png"

    export default {
        name: 'App',
        components: {
            ImageLeftParagraphRight,
            CarouselItem,
            Card,
            IconText2,
            TealTitle,
            MainTitle,
            Paragraph
        },
        data: function () {
            return {
                main_title: {
                    title1: "Understanding the context first, \n" +
                        "then design for it.",
                    title2: "Evaluative Research"
                },
                paragraph: {
                    p1: "In the 8-month project, we spent more than 2 months working on user-centered research to understand our stakeholders’ goals and needs. We invited people from MindEdge, the potential customers and users to help us define our design goals.",
                    p2: "To design a good online learning mobile app for adult learners, we need to learn about the problem space as much as possible. Our goal for evaluative research is to\tunderstand the current market for mobile educational technologies, investigate how learners are engaging with the current content of MindEdge products and identify design principles to guide the future phases.",
                    p3: ""
                },
                carousel_item: {
                    slide_number: 1,
                    c1: {
                        title: "01 Chunked Courses",
                        paragraph: "Segmenting information, especially in the mobile setting, it is important to split instructional content into chunks for learners to digest with minimal risk of cognitive overload.\n",
                        pencil_array: ["Single topic in a paragraph", "Arranged in short-time spans"],
                        img_src: four_cube
                    },
                    c2: {
                        title: "02 Chunked Courses",
                        paragraph: "It is important to design how will learners interact with content like exercise,  feedback, nudging information and so on.\n",
                        pencil_array: ["Practical exercises", "Hands-on tasks", "Instant feedback"],
                        img_src: pointer
                    },
                    c3: {
                        title: "03 Continued Access",
                        paragraph: "Learners need to easily access the content from different channels.\n",
                        pencil_array: ["Cloud computing file storage", "Track learning progress", "Offline services"],
                        img_src: screens
                    },
                    c4: {
                        title: "04 Flexible Pedagogies",
                        paragraph: "The instructional material needs to satisfy learners with different prior knowledge and pace.\n",
                        pencil_array: ["Different media formats", "Gamified activities", "Multiple, flexible learning paths"],
                        img_src: toss_up
                    }
                },

                card: {
                    lit_review: {
                        number: "30+",
                        title: "Literature Reviews",
                        text: "We reviewed 31 academic papers in the domain of adult learner, mobile learning, and adaptivity. From this literature, we synthesized insights and design principles to guide our ideation phase."
                    },
                    comp_analysis: {
                        number: "10+",
                        title: "Competitive Analysis",
                        text: "We reviewed 13 mobile products to extract common features they have. These common features can serve as a design guide for the ideation and design phase."
                    },
                    elearning: {
                        number: "9",
                        title: "E-learning Principles Evaluations",
                        text: "We analyzed MindEdge’s For-Credit courses using principles from Clark and Mayer’s E-learning and the science of instruction. "
                    },
                    log_data: {
                        number: "1000+",
                        title: "Log Data Analysis",
                        text: "We received a dataset consisting of around 1000 Mindedge students. Through analyzing these data, we aimed at understanding how different variables are affecting test scores and final completion rate. "
                    },
                    cta: {
                        number: "10",
                        title: "Cognitive Task Analysis",
                        text: "Cognitive Task Analysis (CTA) is the study of understanding implicit cognitive activities. We selected 5 math problems  from the MindEdge GED math course and conducted think-alouds with 4 experts  and 6 novices by asking them to verbalize their problem solving process."
                    },
                    interviews: {
                        number: "15",
                        title: "Semi-structured Interviews",
                        text: "We conducted interviews with 5 students, 6 instructors, 2 faculty members, 2 administrators, and 4 MindEdge employees to identify gaps and opportunities they are facing in the space of online learning. \n"
                    },
                    affinity_diagram: {
                        number: "10",
                        title: "Insights from Affinity Diagram",
                        text: "Insights are interpretations of our observations by asking the question why. To interpret is to “see into” a situation or understand the “inner nature” of what we observe. We generated 10 key insights from interviews by using affinity diagram."
                    },
                },
                bulletList: {
                    chunked_courses: ["Single topic in a paragraph", "Arranged in short-time spans"]
                },
                iconText: {
                    // iconText1
                    chunked_courses: {
                        title: "Chunked Courses",
                        text: "Segmenting information, especially in the mobile setting, it is important to split instructional content into chunks for learners to digest with minimal risk of cognitive overload.\n",
                        icon: image46,
                        pencilBullet: {
                            list_text: ["Single topic in a paragraph", "Arranged in short-time spans"]
                        }
                    },
                    interactive_micro: {
                        title: "Interactive Micro-Content",
                        text: "It is important to design how will learners interact with content like exercise,  feedback, nudging information and so on.",
                        icon: image47,
                        pencilBullet: {
                            list_text: ["Practical exercises", "Hands-on tasks", "Instant feedback"]
                        }
                    },
                    continued_access: {
                        title: "Continued Access",
                        text: "Learners need to easily access the content from different channels.\n",
                        icon: image48,
                        pencilBullet: {
                            list_text: ["Cloud computing file storage", "Track learning progress", "Offline services"]
                        }
                    },
                    flexible_pedagogies: {
                        title: "Flexible Pedagogies",
                        text: "The instructional material needs to satisfy learners with different prior knowledge and pace.\n",
                        icon: image49,
                        pencilBullet: {
                            list_text: ["Different media formats", "Gamified activities", "Multiple, flexible learning paths"]
                        }
                    },
                    // iconText1 without list
                    extra_effort: {
                        title: "Instructors require extra effort",
                        text: "Instructors' extra effort in delivering accurate information, providing personal connection and class management is crucial to student success but is demanding\n",
                        icon: image50,
                        pencilBullet: {
                            list_text: []
                        }
                    },
                    challenges: {
                        title: "Instructors desire real world challenges",
                        text: "Instructors desire real-world challenges and practices that are beyond traditional textbooks\n",
                        icon: image51,
                        pencilBullet: {
                            list_text: []
                        }
                    },
                    long_term: {
                        title: "Learners motivated by long-term success",
                        text: "Learners are motivated more by long-term real-life success than short-term learning outcomes\n",
                        icon: image52,
                        pencilBullet: {
                            list_text: []
                        }
                    },
                    flexibility: {
                        title: "Students need for more flexibility is burdensome",
                        text: "Students' needs of flexibility add more burden onto their self-regulation skills\n",
                        icon: image53,
                        pencilBullet: {
                            list_text: []
                        }
                    },
                    // iconText2
                    personal_commitment: {
                        title: "Personal commitments drives students away from learning",
                        text: "Students who are married, employed, remotely located, or older have a higher attrition rate than younger students since they prioritize personal commitments over distance education.\n",
                        icon: image1
                    },
                    course_design: {
                        title: "Course Design is critical to student success",
                        text: "Students’ lack of interest, inability to understand course materials, lack of prerequisite knowledge and low concentration on study hinders learning the most.\n",
                        icon: image2
                    },
                    personalization: {
                        title: "Personalization is crucial for mobile learning",
                        text: "Among the  various mobile learning patents, the most popular ones were those that supported personalized content with multi-device and seamless learning capabilities.\n",
                        icon: image3
                    },
                },
                tab_content: {
                    instructor: {
                        row_1: {
                            instructor_input: instructor_input,
                            instructor_input_title: "Instructor’s input is highly demanded ",
                            instructor_input_paragraph: "Instructors' extra effort in delivering accurate information, providing personal connection and class management is crucial to student success but is demanding\n"
                        },
                        row_2: {
                            realworld_challenge: realworld_challenge,
                            realworld_challenge_title: "Instructors desire real world challenges",
                            realworld_challenge_paragraph: "Instructors desire real-world challenges and practices that are beyond traditional textbooks."
                        }
                    },
                    learners:{
                        row_1:{
                            image: long_term,
                            title: "Learners motivated by long-term success",
                            paragraph: "Learners are motivated more by long-term real-life success than short-term learning outcomes."
                        },
                        row_2:{
                            image: flexibility,
                            title: "Learners need more flexibility",
                            paragraph: "Students' needs of flexibility add more burden onto their self-regulation skills."
                        }
                    }
                },
                image: {
                    double_diamond: double_diamond,
                    design_thinking: design_thinking,
                    carousel_arrow_right: carousel_arrow_right,
                    carousel_arrow_left: carousel_arrow_left,
                    // carousel_slide_1: carousel_slide_1,
                    // carousel_slide_2: carousel_slide_2
                },
            }
        },
        methods: {
            advanceCarouselLabels: function () {
                console.log("carousel advanced")
                return null;
            },
            carousel_prev: function () {
                if (this.carousel_item.slide_number > 1) {
                    $('#carousel-label-' + this.carousel_item.slide_number).removeClass('font-weight-bold');
                    this.carousel_item.slide_number--;
                    $('#carousel-label-' + this.carousel_item.slide_number).addClass('font-weight-bold');
                }
            },
            carousel_next: function () {
                if (this.carousel_item.slide_number < 4) {
                    $('#carousel-label-' + this.carousel_item.slide_number).removeClass('font-weight-bold');
                    this.carousel_item.slide_number++;
                    $('#carousel-label-' + this.carousel_item.slide_number).addClass('font-weight-bold');
                }
            }
        },
        updated() {

            console.log("carousel bold added");
        }
    }

    //    regular javascript
    $('#research_carousel').on('slid.bs.carousel', function () {
        console.log("carousel slides");
    })
</script>

<style scoped>
    #carousel-slide-labels {
        font-family: Lato, sans-serif;
        font-style: normal;
        font-weight: 300;
        font-size: 20px;
        line-height: 24px;
    }

    .carousel-inner {
        background: #FFFFFF;
        box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.25);
        border-radius: 10px;
        height: 40vh;
    }

    .carousel-item {
        height: fit-content;
    }

    .carousel-control-prev {
        align-items: flex-start;
    }

    .carousel-control-next {
        align-items: flex-end;; /* Aligns it at the bottom */
    }

    .nav-tabs{
        border: 0px;
    }

    .nav-item {
        border-right: none;
        border-width: 1px;
        border-color: gray;
        border-radius: 10px 0px 0px 10px;
        box-shadow:  -4px 0px 10px #bbbbbb,
        -5px 0px 5px #bbbbbb, -4px 0px 10px #bbbbbb;
        font-family: Lato, sans-serif;
        font-style: normal;
        font-weight: 300;
        font-size: 16px;
        line-height: 19px;
    }

    #myTabContent {
        box-shadow:  0px 0px 5px #bbbbbb,
        0px 0px 5px #bbbbbb, 0px 0px 5px #bbbbbb;
        height: 40vh;
        border-radius: 10px;
    }

    ul.col-2{
        padding-right:0;
    }
</style>
