<template>
    
</template>

<script>
    export default {
        name: "OverviewPage"
    }
</script>

<style scoped>
    .img-responsive {
        width: 100%;
    }

    .backgroundTop {
        align-items: flex-start;
        /*display: flex;*/
    }

    .backgroundF9F8FF {
        background-color: #F9F8FF;
    }

    /*#backgroundWaveTop{*/
    /*    position: sticky;*/
    /*    top: 2rem;*/
    /*}*/

    img.background {
        width: 100%;
        height: 200px;
        object-fit: fill;
    }


    /*TODO slide*/
    .slide-enter-active {
    }

    .slide-leave-active {
    }

    .slide-leave-to {
    }

    .slide-enter {
    }

    /*TODO adjust slide animation*/
    /* Enter and leave animations can use different */
    /* durations and timing functions.              */
    .slide-fade-enter-active {
        transition: all .5s ease-in-out;
        transition-delay: .5s;
        /*transition: all .3s ease;*/
    }

    .slide-fade-leave-active {
        /*transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);*/
        transition: all .5s ease-in;

    }

    .slide-fade-leave-to
        /* .slide-fade-leave-active below version 2.1.8 */
    {
        transform: translateY(-100vh);
        /*opacity: 0;*/
    }

    .slide-fade-enter {
        transform: translateY(90vh);
        /*opacity: 0;*/
    }

</style>