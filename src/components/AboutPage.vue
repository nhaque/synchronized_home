<template>
    <div>
        <table>
            <tr id="team-introduction"
                :style="{
                backgroundImage: `url(${image.bg1})`,
             'background-repeat': 'no-repeat', 'background-size': '100% 100%'
            }">
                <td class="align-middle justify-content-center">
                    <div class="row my-2">
                        <TealTitle class="col-12" title="Who are we?"></TealTitle>
                    </div>
                    <div class="row my-3">
                        <MainTitle class="col-12" :title="titles.title1"></MainTitle>
                    </div>
                    <div class="row text-justify mb-5">
                        <p class="col my-1">
                            We are five thinkers from Carnegie Mellon University who are improving mobile learning
                            experience
                            based
                            on learning science, cognitive model, user-centered research and design thinking.
                        </p>
                    </div>
                    <div class="row justify-content-center">
                        <div class="col-12">
                            <img id="team-img" :src="image.team">
                        </div>
                    </div>
                </td>
            </tr>


            <tr id="team-member-introduction"
                :style="{
                backgroundImage: `url(${image.bg2})`,
             'background-repeat': 'no-repeat', 'background-size': 'cover'
            }">
                <td class="align-middle justify-content-center">
                    <div class="py-1">
                        <div class="container">
                            <div class="row my-6">
                                <div class="row my-5">
                                    <MainTitle class="col-12" :title="titles.title2"></MainTitle>
                                </div>
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
                </td>
            </tr>


            <tr id="team-logo"
                :style="{
                backgroundImage: `url(${image.bg3})`,
             'background-repeat': 'no-repeat', 'background-size': '100% 100%'
            }">
                <td class="align-middle justify-content-center">
                    <div class="row">
                        <TealTitle class="col-12" title="Our logo"></TealTitle>
                    </div>
                    <div class="row">
                        <MainTitle class="col-12" :title="titles.title3"></MainTitle>
                    </div>
                    <div class="container py-3">


                        <div class="row my-2">
                            <div class="col-8 my-2">
                                <ul>
                                    <div class="row my-2">
                                        <li class="col my-3">
                                            The team name consists of the initials of the team members’ names: S is from
                                            Shujing, Y
                                            is from Yu, N is from Nabeeha, C is from Congying, H is from Henry, and ED
                                            is from
                                            education!
                                        </li>
                                    </div>

                                    <div class="row my-3">
                                        <li class="col my-1">
                                            Blue is our favorite color
                                        </li>
                                    </div>

                                    <div class="row my-3">
                                        <li class="col my-1">
                                            The paralleled cloud means the synchrony of the team members
                                        </li>
                                    </div>

                                    <div class="row my-3">
                                        <li class="col my-1">
                                            The sky and cloud implies the bright future of the project and our team
                                            members
                                        </li>
                                    </div>

                                    <div class="row my-3">
                                        <li class="col my-1">
                                            Also, the cloud looks like a ‘thumb up’ 👍
                                        </li>
                                    </div>

                                    <div class="row my-3">
                                        <li class="col my-1">
                                            It doesn’t mean synchronous learning!
                                        </li>
                                    </div>
                                </ul>
                            </div>

                            <div class="col-4 my-3">
                                <img :src="image.team_logo">
                            </div>
                        </div>
                    </div>
                </td>
            </tr>
        </table>
    </div>

</template>

<script>
    import TealTitle from "@/components/TealTitle";
    import MainTitle from "./MainTitle";
    import Introduction from "./Introduction";
    import shujing from "./images/shujing.png";
    import congying from "./images/congying.png";
    import yu from "./images/yu.png";
    import nabeeha from "./images/nabeeha.png";
    import henry from "./images/henry.png";
    import team from "./images/team.png";
    import team_logo from "./images/teamlogo.png";
    import team_bg_1 from "./images/team-bg1.png";
    import team_bg_2 from "./images/team-bg-2.png";
    import team_bg_3 from "./images/team-bg-3.png";

    export default {
        name: 'AboutPage',
        components: {
            Introduction,
            TealTitle,
            MainTitle
        },
        data: function () {
            return {
                titles: {
                    title1: "Hi, We are Team SynchronizED!",
                    title2: "Meet the Team",
                    title3: "Brand Design"
                },
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
                    team_logo: team_logo,
                    bg1: team_bg_1,
                    bg2: team_bg_2,
                    bg3: team_bg_3
                }
            }
        }
    }
</script>

<style>
    tr {
        height: 100vh
    }

    #team-introduction {
        height: 120vh;
    }

    #team-member-introduction {
        height: 120vh;
    }

    #team-logo {
        height: 120vh;
    }

    .mt-6,
    .my-6 {
        margin-top: 8rem !important;
    }

    .mb-6,
    .my-6 {
        margin-bottom: 8rem !important;
    }


    #team-img {
        width: 100%;
        height: auto;
        filter: drop-shadow(0px 0px 15px rgba(0, 0, 0, 0.25));
        border-radius: 10px;
    }






</style>