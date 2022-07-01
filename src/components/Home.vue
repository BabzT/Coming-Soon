<template>
    <div class="body">
        <div>
            <img src="../assets/img.png" alt="">
        </div>
        <h1 class="heading">COMING SOON</h1>
        <CountDown/>
        <FooterSection/>
    </div>
</template>

<script>
import CountDown from './CountDown.vue'
import FooterSection from './Footer.vue'
    export default {
        name: 'HomePage',
        components:{
            CountDown,
            FooterSection,
        }
    }
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.body{
    background-color: #f9f9f9;
    height: 80%;
    width: 80%;
    /* border: 1px solid red; */
    padding: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
}

.heading{
    color: #FFCE27;
    font-style: normal;
    font-size: 50px;
}

@media screen and (max-width: 960px) {
    .heading{
    color: #FFCE27;
    font-style: normal;
    font-size: 38px;
}
}

@media screen and (max-width: 768px) {
    .body{
    height: 85%;
    width: 90%;
}

    .heading{
    margin-bottom: 25px;
    font-size: 22px;
}
}


</style>