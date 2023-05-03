
<script>

    import AppList from "../components/AppList.vue"

    export default{
        name: "AppMain",
        components: {
            AppList,  
        },

        data(){
            return{

                iconsList: [
                    {
                        nome: 'DIGITAL COMICS',
                        img: '/images/buy-comics-digital-comics.png',
                        link: '/comics',
                    },
                    {
                        nome: 'DC MERCHANDISE',
                        img: '/images/buy-comics-merchandise.png',
                        link: '/merchandise',
                    },
                    {
                        nome: 'SUBSCRIPTION',
                        img: './images/buy-comics-subscriptions.png',
                        link: '/subscription',
                    },
                    {
                        nome: 'COMIC SHOP LOCATOR',
                        img: '/images/buy-comics-shop-locator.png',
                        link: '/shop',
                    },
                    {
                        nome: 'DC POWER VISA',
                        img: '/images/buy-dc-power-visa.svg',
                        link: '/visa',
                    }
                ]

            }
        }
    }

</script>

<template>

    <main>

        <div class="content">
            <p> -- Content goes here -- </p>
        </div>

        <div class="listIcons">
            <ul>
                <li v-for="(element, index) in iconsList" :key="iconsList">
                    <img v-bind:src="element.img" alt="">
                    <a href="element.link">{{ element.nome }} </a>
                </li>
            </ul>
        </div>

        <AppList/>

    </main>

</template>

<style scoped lang="scss">
    .content{
        background-color: black;

        p{
            font-size: 1.5rem;
            color: white;
            padding: 2rem 0;
            width: 70%;
            margin: auto;
        }
    }

    .listIcons{
        background-color: #0282f9;
        height: 7rem;
        display: flex;
        align-items: center;
        justify-content: center;

        ul{
            display: flex;


            li{
                margin: 0 1.5rem;

                a{
                    color: white;
                    font-size: 0.8rem;
                }

                img{
                    height: 2.5rem;
                    vertical-align: middle;
                    margin-right: 10px;
                }
            }
        }
    }



</style>