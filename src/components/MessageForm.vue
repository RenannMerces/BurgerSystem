<template>
    <div class="message-container">
        <p>{{ msg }}</p>
    </div>
</template>

<script>

    export default {
        name: 'MessageForm',
        data() {
            return {
              
            }
        },
        props: {
            msg: String,
        }
    }

</script>

<style scoped>

.message-container{
    justify-content: center;
    align-content: center;
    background-color: #cce5ff;
    color: #004085;
    border: 2px solid #b8daff;
    padding: 10px;
    margin: 30px auto;
    max-width: 450px;
    border-radius: 5px;
}

</style>