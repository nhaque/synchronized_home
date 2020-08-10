<template>
    <div>
        <div id="app" class="container-fluid">
            <div class="row justify-content-center">
                <Navbar :about_page="about_page" :research_page="research_page" v-on:changeView="changeView"></Navbar>
            </div>
            <div id="main-content" class="">
                <div id="about_page" class="row justify-content-center">
                    <AboutPage v-if="about_page==current_page"></AboutPage>
                </div>
                <div id="research_page" class="row justify-content-center">
                    <ResearchPage v-if="current_page==research_page"></ResearchPage>
                </div>
                <div id="ideation_page" class="row justify-content-center">
                    <IdeationPage name="IdeationPage" v-if="current_page==ideation_page"></IdeationPage>
                </div>
                <div id="prototype_page" class="row justify-content-center">
                    <PrototypePage name="PrototypePage" v-if="current_page==prototype_page"></PrototypePage>
                </div>
                <div id="overview_page" class="row justify-content-center">
                    <OverviewPage name="OverviewPage" v-if="current_page==overview_page"></OverviewPage>
                </div>
            </div>
            <Footer></Footer>
        </div>

    </div>


</template>

<script>
    import AboutPage from "./components/AboutPage";
    import ResearchPage from "./components/ResearchPage";
    import Navbar from "@/components/Navbar";
    import Footer from "@/components/Footer";
    import IdeationPage from "@/components/IdeationPage";
    import PrototypePage from "./components/PrototypePage";
    import OverviewPage from "./components/OverviewPage";


    export default {
        name: 'App',
        components: {
            PrototypePage,
            AboutPage,
            ResearchPage,
            IdeationPage,
            OverviewPage,
            Navbar,
            Footer,
        },
        data: function () {
            return {
                current_page: 4,
                about_page: 0,
                research_page: 1,
                ideation_page: 2,
                prototype_page: 3,
                overview_page: 4
            }
        },
        methods: {
            goToResearchPage: function () {
                this.current_page = 1
            },
            changeView: function (page) {
                this.current_page = page
            }
        }
    }
</script>

<style>

    .container-fluid {
        margin: 0 0vw 0 0vw;
        width: 100vw;
        background-color: #FFFFFF;
        padding: 0;
    }

    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: left;
        color: #2c3e50;
    }

    tr {
        height: 110vh;
    }



    td {
        padding: 0 20%;
    }

    div h2 {
        font-family: Proxima Nova, Helvetica, sans-serif;
        font-style: normal;
        font-weight: bold;
        font-size: 28px;
        line-height: 34px;
        display: flex;
        align-items: center;

        color: #000000;
    }

    div h6 {
        font-family: Proxima Nova, Helvetica, sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 20px;
        line-height: 26px;
        color: #000000;
    }


    div h3 {
        font-family: Libre Baskerville, Helvetica, sans-serif;
        font-style: normal;
        font-weight: bold;
        font-size: 20px;
        line-height: 140%;

        color: #0081B8;
    }


    p {
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 20px;
        line-height: 28px;


        color: #000000;
    }

    ul {
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 20px;
        line-height: 26px;

        color: #111111;
    }

    ul li::before {
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 20px;
        line-height: 26px;

        color: #2F80ED;
    }


    img {
        max-width: 100%
    }
</style>
