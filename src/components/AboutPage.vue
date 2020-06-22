<template>
    <div>
        <div class="container">
            <div class="row my-2">
                <h2 class="col">Hi, We are Team SynchronizED!</h2>
            </div>
            <div class="row">
                <p class="col my-1">
                    We are five thinkers from Carnegie Mellon University who are improving mobile learning experience
                    based
                    on learning science, cognitive model, user-centered research and design thinking.
                </p>
            </div>
            <div class="row text-center my-5">
                <div class="col-md-12 col-sm-12 pl-0 my-1">
                    <img id="team-img" :src="image.team">
                </div>
            </div>
        </div>

            <div class="team-member  py-5">
                <div class="container" id = "intro">
                    <div class="row justify-content-center my-6">
                        <div class="col-md-12 col-sm-12">
                            <Introduction :name="introduction.shujing.name" :role="introduction.shujing.role"
                                          :intro_text="introduction.shujing.intro"
                                          :image="introduction.shujing.image"></Introduction>
                        </div>
                    </div>

                    <div class="row justify-content-center my-6">
                        <div class="col-md-12 col-sm-12">
                            <Introduction :name="introduction.yu.name" :role="introduction.yu.role"
                                          :intro_text="introduction.yu.intro"
                                          :image="introduction.yu.image"></Introduction>
                        </div>
                    </div>

                    <div class="row justify-content-center my-6">
                        <div class="col-md-12 col-sm-12">
                            <Introduction :name="introduction.nabeeha.name" :role="introduction.nabeeha.role"
                                          :intro_text="introduction.nabeeha.intro"
                                          :image="introduction.nabeeha.image"></Introduction>
                        </div>
                    </div>


                    <div class="row justify-content-center my-6">
                        <div class="col-md-12 col-sm-12">
                            <Introduction :name="introduction.congying.name" :role="introduction.congying.role"
                                          :intro_text="introduction.congying.intro"
                                          :image="introduction.congying.image"></Introduction>
                        </div>
                    </div>

                    <div class="row justify-content-center my-6">
                        <div class="col-md-12 col-sm-12">
                            <Introduction :name="introduction.henry.name" :role="introduction.henry.role"
                                          :intro_text="introduction.henry.intro"
                                          :image="introduction.henry.image"></Introduction>
                        </div>
                    </div>
                </div>
            </div>


            <div class="container py-5">
                <div class="row my-2">
                    <h2 class="col">Logo Design</h2>
                </div>

                <div class="row my-2">
                    <div class="col-8 my-2">
                        <ul>
                            <div class="row my-2">
                                <li class="col my-1">
                                    The team name consists of the initials of the team members’ names: S is from
                                    Shujing, Y
                                    is from Yu, N is from Nabeeha, C is from Congying, H is from Henry, and ED is from
                                    education!
                                </li>
                            </div>

                            <div class="row my-2">
                                <li class="col my-1">
                                    Blue is our favorite color
                                </li>
                            </div>

                            <div class="row my-2">
                                <li class="col my-1">
                                    The paralleled cloud means the synchrony of the team members
                                </li>
                            </div>

                            <div class="row my-2">
                                <li class="col my-1">
                                    The sky and cloud implies the bright future of the project and our team members
                                </li>
                            </div>

                            <div class="row my-2">
                                <li class="col my-1">
                                    Also, the cloud looks like a ‘thumb up’ 👍
                                </li>
                            </div>

                            <div class="row my-2">
                                <li class="col my-1">
                                    It doesn’t mean synchronous learning!
                                </li>
                            </div>
                        </ul>
                    </div>

                    <div class="col-4 my-2">
                        <img :src="image.team_logo">
                    </div>
                </div>
            </div>
        </div>

</template>

<script>
    import Introduction from "./Introduction";
    import shujing from "./images/shujing.png";
    import congying from "./images/congying.png";
    import yu from "./images/yu.png";
    import nabeeha from "./images/nabeeha.png";
    import henry from "./images/henry.png";
    import team from "./images/team.png";
    import team_logo from "./images/teamlogo.png";

    export default {
        name: 'AboutPage',
        components: {
            Introduction
        },
        data: function () {
            return {
                introduction: {
                    shujing: {
                        image: shujing,
                        name: "Shujing Lin",
                        role: "Research Lead",
                        intro: "Shujing is interested in exploring the world and embracing different cultures, which motivated her to pursue an undergraduate degree in Italian. She has two years of experience in teaching Italian and piano. She is passionate about education and is looking forward to designing engaging and effective learning experience. She is a huge Disney fan."
                    },
                    yu: {
                        image: yu,
                        name: "Yu Zhao",
                        role: "Project Manager",
                        intro: "Yu’s undergraduate degree in psychology allows her to use scientific methods to understand human cognitive and learning processes. She is passionate about bridging learning science and user experience to bring successful projects. She is a huge Pixar fan."
                    },
                    nabeeha: {
                        image: nabeeha,
                        name: "Nabeeha Fatima",
                        role: "Development Lead",
                        intro: "Nabeeha is passionate about building platforms with interactions and innovative tech to meet industry needs and enhance learner experience. Prior to METALS, she worked as a front-end developer and UX lead in Qatar. In her spare time, she is a a tea connoisseur and a novice board gamer."
                    },
                    henry: {
                        image: henry,
                        name: "Henry Chang",
                        role: "Product Manager",
                        intro: "Henry is all about building engaging learning products that attract and help a broad range of learners. He believes with his technical skills and the learning science principles learned in the METALS program, he can reach learners who traditionally have difficulties in accessing high-quality education."
                    },
                    congying: {
                        image: congying,
                        name: "Congying Zhang",
                        role: "Design Lead",
                        intro: "Congying is a UX designer who loves solving problems with innovative ideas, and always keeps the image of the end user in mind. She is excited to apply the learning theory and design principles learned from METALS program to improve educational experiences. She fell in love with Animal Crossing recently."
                    }
                },
                image: {
                    team: team,
                    team_logo: team_logo
                }
            }
        }
    }
</script>

<style>
    .mt-6,
    .my-6 {
        margin-top: 8rem !important;
    }

    .mb-6,
    .my-6 {
        margin-bottom: 8rem !important;
    }


    .team-member {
        background-color: #F4F4F4;
    }

    #team-img {
        width: 100%;
        height: auto;
    }

    #intro {
        background-color: #F4F4F4;
    }
</style>