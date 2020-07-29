<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light nav-justified justify-content-between">
        <a class="navbar-brand" href="#">Logo</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup"
                aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
<!--        <form class="form-inline" id="navbarNavAltMarkup">-->
<!--            <ul class="navbar-nav">-->
<!--                <li class="nav-item nav-link" href="#">Overview<span class="sr-only">(current)</span></li>-->
<!--                &lt;!&ndash;                <a class="nav-item nav-link" href="#">Product</a>&ndash;&gt;-->
<!--                &lt;!&ndash;                <a class="nav-item nav-link disabled" href="#">Disabled</a>&ndash;&gt;-->
<!--                <li class="nav-item nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink"-->
<!--                    data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">-->
<!--                    Process-->
<!--                    <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">-->
<!--                        <a class="dropdown-item" href="#" @click="goToResearchPage">Research</a>-->
<!--                        <a class="dropdown-item" href="#">Ideation</a>-->
<!--                        <a class="dropdown-item" href="#">Prototyping</a>-->
<!--                    </div>-->
<!--                </li>-->
<!--                <li class="nav-item nav-link" href="#" @click="goToResearchPage">About</li>-->
<!--            </ul>-->
        <ul class="navbar-nav">
            <li class="nav-item active">
                <a class="nav-link" href="#">Overview <span class="sr-only">(current)</span></a>
            </li>
            <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                    Process
                </a>
                <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                    <a class="dropdown-item" href="#" @click="goToResearchPage">Research</a>
                    <a class="dropdown-item" href="#">Ideation</a>
                    <a class="dropdown-item" href="#">Prototyping</a>
                </div>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="#">About</a>
            </li>

        </ul>
<!--        </form>-->
    </nav>
</template>

<script>
    export default {
        name: "Navbar",
        props: {
            about_page: Boolean,
            research_page: Boolean
        },
        methods: {
            goToResearchPage: function () {
                this.$emit('changeView')
            }
        }
    }
</script>

<style scoped>
    .nav-item {
        font-family: Proxima Nova;
        font-style: normal;
        font-weight: normal;
        font-size: 18px;
        line-height: 22px;
        display: flex;
        align-items: center;

        color: #000000;
    }
</style>