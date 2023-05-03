<script>

    export default{
        name: "AppHeader",

        data(){
            return{

                headerList: [
                    {
                        nome: "CHARACTERS",
                        path: "/characters",
                        active: false,
                    },
                    {
                        nome: "COMICS",
                        path: "/comics",
                        active: true,
                    },
                    {
                        nome: "MOVIES",
                        path: "/movies",
                        active: false,
                    },
                    {
                        nome: "TV",
                        path: "/tv",
                        active: false,
                    },
                    {
                        nome: "GAMES",
                        path: "/games",
                        active: false,
                    },
                    {
                        nome: "COLLECTIBLES",
                        path: "/collectibles",
                        active: false,
                    },
                    {
                        nome: "VIDEOS",
                        path: "/videos",
                        active: false,
                    },
                    {
                        nome: "FANS",
                        path: "/fans",
                        active: false,
                    },
                    {
                        nome: "NEWS",
                        path: "/news",
                        active: false,
                    },
                    {
                        nome: "SHOP",
                        path: "/shop",
                        active: false,
                    },
                ]

            }
        }
    }

</script>

<template>

    <header>
        <nav>

            <div>
                <img src="/images/dc-logo.png" alt="logo dc">
            </div>


            <div>
                <ul>
                    <li v-for="(element, index) in headerList">
                        <a href="element.path">{{ element.nome }} </a>
                    </li>
                </ul>
            </div>

        </nav>
    </header>

</template>

<style scoped lang="scss">

    nav{
        display: flex;
        justify-content: space-around;
        align-items: center;

        ul{
            display: flex;

            li{
                margin: 0 0.5rem;
                font-size: 0.8rem;
                padding: 2.5rem 0;
            }
        }
    }

    img{
        height: 4rem;
    }

</style>
