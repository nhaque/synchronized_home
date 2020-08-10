<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light nav-justified justify-content-between fixed-top">
        <a class="navbar-brand ml-5" href="#">logo</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup"
                aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <ul class="navbar-nav mr-5">
            <li class="nav-item active">
                <a class="nav-link" href="#" @click="goToOverviewPage">Product<span class="sr-only">(current)</span></a>
            </li>
            <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                    Process
                </a>
                <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                    <a class="dropdown-item" href="#" @click="goToResearchPage">Research</a>
                    <a class="dropdown-item" href="#" @click="goToIdeationPage">Ideation</a>
                    <a class="dropdown-item" href="#" @click="goToPrototypePage">Prototyping</a>
                </div>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="#" @click="goToAboutPage">Team</a>
            </li>

        </ul>
    </nav>
</template>



<script>

    export default {
        name: 'Navbar',
        props: {
        },
        methods: {
            goToResearchPage: function () {
                this.$emit('changeView', 1)
            },
            goToIdeationPage: function(){
                this.$emit('changeView', 2)
            },
            goToPrototypePage: function(){
                this.$emit('changeView', 3)
            },
            goToOverviewPage: function(){
                this.$emit('changeView', 4)
            },
            goToAboutPage: function(){
                this.$emit('changeView', 0)
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
    nav{
        height: 94px;
        background: #FFFFFF;
        box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.15);
    }
</style>