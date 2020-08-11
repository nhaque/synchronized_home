<template>
    <nav class="navbar navbar-expand-lg justify-content-between fixed-top">
        <a class="navbar-brand ml-5" href="#" @click="goToOverviewPage"> <b>SynchronizED</b></a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup"
                aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <ul class="navbar-nav mr-5">
            <li id="product" class="nav-item active font-weight-bold">
                <a class="nav-link" href="#" @click="goToOverviewPage">Product<span class="sr-only">(current)</span></a>
            </li>
            <li id="process" class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                    Process
                </a>
                <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                    <a class="dropdown-item" href="#" @click="goToResearchPage">Research</a>
                    <a class="dropdown-item" href="#" @click="goToIdeationPage">Ideation</a>
                    <a class="dropdown-item" href="#" @click="goToPrototypePage">Prototyping</a>
                </div>
            </li>
            <li id="team" class="nav-item">
                <a class="nav-link" href="#" @click="goToAboutPage">Team</a>
            </li>

        </ul>
    </nav>
</template>



<script>

    import pic1 from "@/components/images/teamlogo.png";

    export default {
        name: "Navbar",

        props: {
        },

        components: {
        },

        data: function(){
            return{
                image: {
                    pic: pic1
                }
            }
        },
        methods: {
            goToResearchPage: function () {
                this.$emit('changeView', 1);
                boldItem("process");
            },
            goToIdeationPage: function(){
                this.$emit('changeView', 2);
                boldItem("process");
            },
            goToPrototypePage: function(){
                this.$emit('changeView', 3);
                boldItem("process");
            },
            goToOverviewPage: function(){
                this.$emit('changeView', 4);
                boldItem("product");
            },
            goToAboutPage: function(){
                this.$emit('changeView', 0);
                boldItem("team");
            }
        }
    }

    function boldItem(id) {
        var nav = document.getElementsByClassName("nav-item");
        for(var i = 0; i < nav.length; i++) {
            console.log(i.valueOf());
            nav[i].classList.remove("font-weight-bold");
        }

        var process = document.getElementById(id);
        process.classList += " font-weight-bold";
    }


</script>

<style scoped>
    .nav-item {
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
    .img-responsive{
        height: auto;
        width: auto;
        max-height: 92px;
        max-width: 250px;
    }

    a{
        color:#000000;
    }

    a.hover{
        color:#0081B8;
    }
</style>