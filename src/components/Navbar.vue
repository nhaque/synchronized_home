<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light nav-justified justify-content-between">
        <a class="navbar-brand" href="#">Logo</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <form class="form-inline" id="navbarNavAltMarkup">
            <div class="navbar-nav">
                <a class="nav-item nav-link" href="#">Overview<span class="sr-only">(current)</span></a>
                <a class="nav-item nav-link" href="#">Product</a>
<!--                <a class="nav-item nav-link disabled" href="#">Disabled</a>-->
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                    Process
                </a>
                <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                    <a class="dropdown-item" href="#" @click="goToResearchPage">Research</a>
                    <a class="dropdown-item" href="#">item 2</a>
                    <a class="dropdown-item" href="#">item 3</a>
                </div>
                <a class="nav-item nav-link" href="#" >About</a>
            </div>
        </form>
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
            goToResearchPage: function() {
                this.about_page = false;
                this.research_page = true;
            }
        }
    }
</script>

<style scoped>
    .nav-item.nav-link{
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