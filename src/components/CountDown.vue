<template>
    <div>
        <section class="container">
            <div class="wrapper">
                <div class="label">Days</div>
                <h2 class="digits">{{days < 10 ? "0" + days : days}}</h2>
            </div>
            <span class="column">:</span>

            <div class="wrapper">
                <div class="label">Hours</div>
                <h2 class="digits">{{(hours % 24) < 10 ? "0" + (hours % 24) : (hours % 24)}}</h2>
            </div>
            <span class="column">:</span>

            <div class="wrapper">
                <div class="label">Minutes</div>
                <h2 class="digits">{{(minutes % 60) < 10 ? "0" + (minutes % 60) : (minutes % 60)}}</h2>
            </div>
            <span class="column">:</span>

            <div class="wrapper">
                <div class="label">Seconds</div>
                <h2 class="digits">{{(seconds % 60) < 10 ? "0" + (seconds % 60) : (seconds % 60)}}</h2>
            </div>
        </section>
    </div>
</template>

<script>
import {ref} from '@vue/reactivity'
    export default {
        name: 'CountDown',
        setup(){
            let days = ref(0);
            let hours = ref(0);
            let minutes = ref(0);
            let seconds = ref(0);
            let launchDate = new Date('15 July 2022')

            let timer = setInterval(() => {
                let currDate = new Date();
                let launchTime = launchDate - currDate;

                if(launchTime < 0){
                    clearInterval(timer)
                    return;
                }

                seconds.value = parseInt(launchTime/1000);
                minutes.value = parseInt(seconds.value/60);
                hours.value = parseInt(minutes.value/60) ;
                days.value = parseInt(hours.value/24);
            },1000)
            return{days, hours, minutes, seconds}
        }
        
    }
</script>

<style scoped>
    .container{
        /* border: 1px solid green; */
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }
    
    .label{
        color: #292D32;
        font-size: 23px;
        font-weight: bold;
    }
    .digits{
        color: #F48212;
        font-size: 100px;
        margin: 0 15px;
    }
    .column{
        font-size: 100px;
        margin-top: 20px;
        color: #929292;
    }

    @media screen and (max-width: 960px) {

        .label{
        font-size: 15px;
        font-weight: bold;
    }

        .digits{
        font-size: 50px;
        margin: 0 5px;
    }

    .column{
        font-size: 50px;
        margin-top: 10px;
    }

    @media screen and (max-width: 768px) {
        .container{
        margin-bottom: 50px;
    }
        .label{
        font-size: 10px;
        margin-bottom: 10px;
        font-weight: bold;
    }

        .digits{
        font-size: 30px;
        margin: 0 5px;
    }

    .column{
        font-size: 30px;
        margin-top: 17px;
    }
    }
    }
</style>