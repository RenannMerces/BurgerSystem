<template>
    <div id="main-banner">
        <h1>Make Your Burger</h1>
    </div>
</template>

<script>
    export default {
        name: 'BannerHome',
    }
</script>

<style scoped>
    #main-banner{
        background-image: url('/public/img/burger.jpg');
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        min-height: 700px;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: flex-start;
    }

    #main-banner h1{
        color: #fcba26;
        font-size: 60px;
        margin-left: 50px;
        text-align: center;
        background-color: #222;
        padding: 20px 40px;
    }

</style>