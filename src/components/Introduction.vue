<template>
    <div class="introduction">
            <div class="row align-items-center pl-0">
            <div class="col-3 mr-5 intro_image">
                <img :src="image">
            </div>
            <div class="col-8 d-flex justify-content-between flex-column  introduction-body">
                <div class="row name_role my-4" >
                    <div class="col introduction-name">
                        {{name}}
                    <span class="col introduction-role pl-0">
                        | {{role}}
                    </span>
                    </div>
                </div>
                <div class="row introduction-text mb-4">
                    <div class="col-md-12 col-lg-12">
                        {{intro_text}}
                    </div>
                </div>
                <div class="row contact">
                    <div class = "col">
                    <a :href="resume" target="_blank" class="resume">
                        Resume
                    </a>
                    |
                    <a :href="linkedIn" target="_blank" class="linkedIn">
                        LinkedIn
                    </a>
                    |
                    <a :href="portfolio" target="_blank" class="portfolio">
                        Portfolio
                    </a>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
    export default {
        name: "Introduction",
        props: {
            name: String,
            role: String,
            intro_text: String,
            image: String,
            resume: String,
            linkedIn: String,
            portfolio: String,
        }

    }
</script>

<style scoped>
    .introduction {
        /*width: 506px;*/
        /*height: 251px;*/
    }

    .introduction-name {
        font-family: Proxima Nova, sans-serif;
        font-style: normal;
        font-weight: bold;
        font-size: 28px;
        line-height: 28px;
        color: #000000;
    }

    .introduction-role {
        font-family: Proxima Nova, sans-serif;
        font-style: normal;
        font-weight: 300;
        font-size: 28px;
        line-height: 28px;
        color: #5F5F5F;
    }


    .introduction-text {
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 20px;
        line-height: 28px;
        color: #111111;
    }

    .contact {
        font-family: Open Sans， sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 18px;
        line-height: 22px;
        color: #2F80ED;
    }


</style>