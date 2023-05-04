
<script>

    import AppList from "./AppList.vue"
    import AppComics from "./AppComics.vue"

    export default{
        name: "AppMain",
        components: {
            AppList, 
            AppComics 
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
                ],
                

                //lista dei fumetti da inserire nel props
                comics: [
                    {
                        "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                        "price": "$19.99",
                        "series": "Action Comics",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                        "price": "$3.99",
                        "series": "American Vampire 1976",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                        "price": "$16.99",
                        "series": "Aquaman",
                        "type": "graphic novel",
                    },
                    {
                        "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                        "price": "$2.99",
                        "series": "Batgirl",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                        "price": "$3.99",
                        "series": "Batman",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                        "price": "$2.99",
                        "series": "Batman Beyond",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                        "price": "$3.99",
                        "series": "Batman/Superman",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                        "price": "$4.99",
                        "series": "Batman/Superman Annual",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                        "price": "$5.99",
                        "series": "Batman: The Joker War Zone",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                        "price": "$6.99",
                        "series": "Batman: Three Jokers",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                        "price": "$4.99",
                        "series": "Batman: White Knight Presents: Harley Quinn",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                        "price": "$16.99",
                        "series": "Catwoman",
                        "type": "graphic novel",
                    },              
                ]

            }
        }
    }

</script>

<template>

    <main>

        <div class="content">
            <img src="/images/jumbotron.jpg" alt="jumbotron">

            <div class="current-series">
                <span class="series-text">CURRENT SERIES</span>
            </div>
        </div>

        

        <div class="large-container">

            <div class="container">
                <AppComics v-for="(element, index) in comics" 
                :key="index" 
                :singleComic="element"/>
            </div>

            <div class="center">
                <span class="load-more">LOAD MORE</span>
            </div>

        </div>

        <div class="listIcons">
            <ul>
                <li v-for="(element, index) in iconsList" :key="index">
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
        position: relative;

        img{
           height: 20rem; 
           width: 100%;
           object-fit: cover;
           object-position: top;
           margin-bottom: -1em;
        }
    }

    .current-series{
        position: absolute;
        bottom: -1rem;
        left: 10rem;

        .series-text{
            color: white;
            background-color: #0282f9;
            padding: 1rem;
            font-weight: bold;
        }
    }

    .large-container{
        background-color: #1c1c1c;
        padding-bottom: 2rem;
        .container{
            width: 70%;
            margin: auto;
            padding-top: 4rem;
            padding-bottom: 1rem;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .center{
            text-align: center;

            .load-more{
                color: white;
                background-color: #0282f9;
                padding: 1rem 3rem;
                margin-top: 1rem;
                font-size: 0.8rem;
            }
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