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
                <td>
                    <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
                        <div class="carousel-inner">
                            <div class="carousel-item active">
                                <div src="" class="d-block w-100" alt="..."><p>test</p></div>
                            </div>
                            <div class="carousel-item">
                                <div src="" class="d-block w-100" alt="..."><p>test2</p></div>
                            </div>
                            <div class="carousel-item">
                                <div src="" class="d-block w-100" alt="..."><p>test3</p></div>
                            </div>
                        </div>
                        <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
                            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                            <span class="sr-only">Previous</span>
                        </a>
                        <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
                            <span class="carousel-control-next-icon" aria-hidden="true"></span>
                            <span class="sr-only">Next</span>
                        </a>
                    </div>
                </td>
            </tr>

            <div class="row my-3 pl-5">
                <h6>Design Implication Guidelines</h6>
            </div>
            <div class="row justify-content-center">
                <div class="col-md-6 col-sm-12">
                    <IconText1 :icon_text_title="iconText.chunked_courses.title"
                               :icon_text_text="iconText.chunked_courses.text" :img-src="iconText.chunked_courses.icon"
                               :list_texts="iconText.chunked_courses.pencilBullet.list_text"></IconText1>
                </div>
                <div class="col-md-6 col-sm-12">
                    <IconText1 :icon_text_title="iconText.interactive_micro.title"
                               :icon_text_text="iconText.interactive_micro.text"
                               :img-src="iconText.interactive_micro.icon"
                               :list_texts="iconText.interactive_micro.pencilBullet.list_text"></IconText1>
                </div>
            </div>
            <div class="row justify-content-center">
                <div class="col-md-6 col-sm-12">
                    <IconText1 :icon_text_title="iconText.continued_access.title"
                               :icon_text_text="iconText.continued_access.text"
                               :img-src="iconText.continued_access.icon"
                               :list_texts="iconText.continued_access.pencilBullet.list_text"></IconText1>
                </div>
                <div class="col-md-6 col-sm-12">
                    <IconText1 :icon_text_title="iconText.flexible_pedagogies.title"
                               :icon_text_text="iconText.flexible_pedagogies.text"
                               :img-src="iconText.flexible_pedagogies.icon"
                               :list_texts="iconText.flexible_pedagogies.pencilBullet.list_text"></IconText1>
                </div>
            </div>
            <div class="row my-3 pl-5">
                <h6>Key Insights</h6>
            </div>
            <div class="row justify-content-center pl-5">
                <div class="col-md col-sm">
                    <IconText2 :icon_text_title="iconText.personal_commitment.title"
                               :icon_text_text="iconText.personal_commitment.text"
                               :img-src="iconText.personal_commitment.icon"></IconText2>
                </div>
                <div class="col-md col-sm">
                    <IconText2 :icon_text_title="iconText.course_design.title"
                               :icon_text_text="iconText.course_design.text"
                               :img-src="iconText.course_design.icon"></IconText2>
                </div>
                <div class="col-md col-sm">
                    <IconText2 :icon_text_title="iconText.personalization.title"
                               :icon_text_text="iconText.personalization.text"
                               :img-src="iconText.personalization.icon"></IconText2>
                </div>
            </div>
            <div class="row my-3 mt-3">
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
            <div class="row justify-content-center my-5">
                <Card class="col-md-6 col-xs-6 my-1" :quant="card.cta.number" :card_title="card.cta.title"
                      :card_content="card.cta.text"></Card>

                <Card class="col-md-6 col-xs-6 my-1" :quant="card.interviews.number"
                      :card_title="card.interviews.title"
                      :card_content="card.interviews.text"></Card>
                <Card class="col-md-6 col-xs-6 my-1" :quant="card.affinity_diagram.number"
                      :card_title="card.affinity_diagram.title"
                      :card_content="card.affinity_diagram.text"></Card>
            </div>
            <div class="row pl-5">
                <h6>Key Insights</h6>
            </div>
            <div class="row justify-content-center">
                <div class="col-md-6 col-sm-12">
                    <IconText1 :icon_text_title="iconText.extra_effort.title"
                               :icon_text_text="iconText.extra_effort.text" :img-src="iconText.extra_effort.icon"
                               :list_texts="iconText.extra_effort.pencilBullet.list_text"></IconText1>
                </div>
                <div class="col-md-6 col-sm-12">
                    <IconText1 :icon_text_title="iconText.challenges.title"
                               :icon_text_text="iconText.challenges.text" :img-src="iconText.challenges.icon"
                               :list_texts="iconText.challenges.pencilBullet.list_text"></IconText1>
                </div>
            </div>
            <div class="row">
                <div class="col-md-6 col-sm-12">
                    <IconText1 :icon_text_title="iconText.long_term.title"
                               :icon_text_text="iconText.long_term.text" :img-src="iconText.long_term.icon"
                               :list_texts="iconText.long_term.pencilBullet.list_text"></IconText1>
                </div>
                <div class="col-md-6 col-sm-12">
                    <IconText1 :icon_text_title="iconText.flexibility.title"
                               :icon_text_text="iconText.flexibility.text"
                               :img-src="iconText.flexibility.icon"
                               :list_texts="iconText.flexibility.pencilBullet.list_text"></IconText1>
                </div>
            </div>
        </table>
        <Footer></Footer>
    </div>

</template>

<script>
    import Card from "@/components/Card";
    import IconText1 from "@/components/IconText1";
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

    export default {
        name: 'App',
        components: {
            Card,
            IconText1,
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
                    p1: "In the 8-month project, we spent more than 2 months working on user-centered research to understand our stakeholders’ goals and needs. We invited people from MindEdge, the potential customers and users to help us define our design goals."
                    ,
                    p2: "To design a good online learning mobile app for adult learners, we need to learn about the problem space as much as possible. Our goal for evaluative research is to\tunderstand the current market for mobile educational technologies, investigate how learners are engaging with the current content of MindEdge products and identify design principles to guide the future phases.",
                    p3: ""
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
                image: {
                    double_diamond: double_diamond,
                    design_thinking: design_thinking
                },
            }
        }
    }
</script>

<style>
</style>
