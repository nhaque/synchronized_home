<template>
    <div>
        <div id="app" class="container">
            <Navbar></Navbar>
            <div class = "btn btn-primary" @click="goToResearchPage"> research </div>
        </div>
        <AboutPage v-if = "about_page"></AboutPage>
        <div id = "research_page">
        <div id="research" class="container">
            <ResearchPage v-if = "research_page"></ResearchPage>
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


    export default {
        name: 'App',
        components: {
            AboutPage,
            ResearchPage,
            Navbar,
            Footer,
        },
        data: function () {
            return {
                about_page: true,
                research_page: false
            }
        },
        methods: {
            goToResearchPage: function() {
                this.about_page = false;
                this.research_page = true;
            }
        }
    }
</script>

<style>

    .container {
        margin: 0 5vw 0 5vw;
        width: 90vw;
        background-color: #FFFFFF;
    }
yarn

    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: left;
        color: #2c3e50;
        margin-top: 60px;
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
