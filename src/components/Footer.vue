<template>
    <div class="footer">
        <a href="https://www.facebook.com/paramountstudent" class="link">
            <div class="social" >
            <img src="@/assets/fb.png" alt="">
            <p class="socialtext">Facebook</p>
        </div>
        </a>

        <a href="https://www.instagram.com/paramount.students/?hl=en" class="link">
            <div class="social">
            <img src="@/assets/insta.png" alt="">
            <p class="socialtext">Instagram</p>
        </div>
        </a>
        <a href="https://www.linkedin.com/company/paramount-student/mycompany/" class="link">
            <div class="social">
            <img src="@/assets/linked.png" alt="">
            <p class="socialtext">LinkedIn</p>
        </div>
        </a>
        <a href="https://twitter.com/ParamountStds" class="link">
            <div class="social">
            <img src="@/assets/twi.png" alt="">
            <p class="socialtext">Twitter</p>
        </div>
        </a>
    </div>
</template>

<script>
    export default {
        name: 'FooterSection'
    }
</script>

<style scoped>

    .footer{
        /* border: 1px solid red; */
        height: 50px;
        width: 55%;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .link{
        color: black;
        text-decoration: none;
    }

    .social{
        /* border: 1px solid black; */
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .socialtext{
        margin: 0;
        font-size: 15px;
        margin-left: 10px;
    }

    @media screen and (max-width: 960px) {
        .footer{
        height: 50px;
        width: 70%;
    }

    .socialtext{
        margin: 0;
        font-weight: bold;
        font-size: 8px;
        margin-left: 5px;
    }
    }

    @media screen and (max-width: 768px) {
        .footer{
        height: 50px;
        margin-bottom: 30px;
        width: 70%;
    }

    .socialtext{
        display: none;
    }
    }
</style>