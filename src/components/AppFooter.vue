<script>

    export default{
        name: "AppFooter",

        data(){
            return{

                socialMedia: [
                    "/images/footer-facebook.png",
                    "/images/footer-periscope.png",
                    "/images/footer-pinterest.png",
                    "/images/footer-twitter.png",
                    "/images/footer-youtube.png",
                ]

            }
        }
    }

</script>

<template>

    <div class="container">

        <div>
            <div class="sign-up">SIGN-UP NOW!</div>
        </div>

        <div class="social-media">
            <p><strong>FOLLOW US</strong></p>
            <div v-for="(element) in socialMedia" :key="socialMedia">             
                <img v-bind:src="element" alt="icon">
            </div>
        </div>

    </div>

</template>

<style scoped lang="scss">

    .container{
        height: 6rem;
        display: flex;
        justify-content: space-around;
        align-items: center;
        background-color: #303030;

        div{
            .sign-up{
                color: white;
                padding: 0.5rem;
                border: 2px solid #0c7cec;
            }
        }


        .social-media{
            display: flex;
            align-items: center;

            p{
                margin-right: 10px;
                color: #0c7cec;
            }

            div{
                margin: 5px;
            }

        }
    }

</style>