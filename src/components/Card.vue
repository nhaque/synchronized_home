<template>
    <div class="card m-3 p-0 text-left">
        <div class="card-body p-3">
        <div class="row data_quantity">
            <div class="col">
                {{quant}}
            </div>
        </div>
        <div class="row card-title">
            <h5 class="col">{{card_title}}</h5>
        </div>
        <div class="row card-text">
            <div class="col">{{card_content}}</div>
        </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Card",
        props: {
            quant: String,
            card_title: String,
            card_content: String
        }
    }
</script>

<style scoped>
    .card{
        max-width: 220px;
        height: 300px;
        box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.15);
        border-width: 0;
    }

    .data_quantity{
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: 300;
        font-size: 40px;
        line-height: 54px;
        color:#02B1E1;
    }

    .card-title{
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 18px;
        line-height: 25px;
        color: #111111;
    }

    .card-text{
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: 300;
        font-size: 14px;
        line-height: 16px;
        color: #000000;
    }
</style>