<script>

    export default{
        name: "AppList",

        data(){
            return{

                //liste 1-2
                firstLists: [
                    {
                        title: 'DC COMICS',
                        elements: [
                            {
                                nome: 'Characters',
                                link: '/Characters',
                            },
                            {
                                nome: 'Comics',
                                link: '/Comics',
                            },
                            {
                                nome: 'Movies',
                                link: '/Movies',
                            },
                            {
                                nome: 'TV',
                                link: '/tv',
                            },
                            {
                                nome: 'Games',
                                link: '/Games',
                            },
                            {
                                nome: 'Videos',
                                link: '/Videos',
                            },
                            {
                                nome: 'News',
                                link: '/News',
                            },
                        ],
                    },
                    {
                        title: 'SHOP',
                        elements: [
                            {
                                nome: 'Shop DC',
                                link: '/Shop',
                            },
                            {
                                nome: 'Shop DC collectibles',
                                link: '/collectibles',
                            }, 
                        ],
                    }

                ],

                //liste 3-4
                secondLists: [
                    {
                        title: 'DC',
                        elements: [
                            {
                                nome: 'Terms of use',
                                link: '/Terms',
                            },
                            {
                                nome: 'Privacy Policy (New)',
                                link: '/Privacy',
                            },
                            {
                                nome: 'Ad Choices',
                                link: '/Ad',
                            },
                            {
                                nome: 'Advertising',
                                link: '/Advertising',
                            },
                            {
                                nome: 'Jobs',
                                link: '/Jobs',
                            },
                            {
                                nome: 'Subscriptions',
                                link: '/Subscriptions',
                            },
                            {
                                nome: 'Talent Workshops',
                                link: '/Talent',
                            },
                            {
                                nome: 'CPSC certificates',
                                link: '/CPSC',
                            },
                            {
                                nome: 'Ratings',
                                link: '/Ratings',
                            },
                            {
                                nome: 'Shop Help',
                                link: '/Help',
                            },
                            {
                                nome: 'Contact us',
                                link: '/Contact',
                            },
                        ],
                    },
                    {
                        title: 'SITES',
                        elements: [
                            {
                                nome: 'DC',
                                link: '/DC',
                            },
                            {
                                nome: 'MAD Magazine',
                                link: '/Magazine',
                            }, 
                            {
                                nome: 'DC Kids',
                                link: '/Kids',
                            }, 
                            {
                                nome: 'DC Universe',
                                link: '/Universe',
                            }, 
                            {
                                nome: 'DC Power Visa',
                                link: '/Visa',
                            }, 
                        ],
                    }

                ]

            }
        }
    }

</script>

<template>

    <div class="big-container">

        <div class="container">
    
            <div class="lists-1">
                <ul v-for="(element, index) in firstLists" :key="index">
                    <h3>{{ element.title }}</h3>
                    <li v-for="(element, index) in element.elements">
                        <a href="element.link">{{ element.nome }} </a>
                    </li>
                </ul>
            </div>
    
            <div class="lists-2">
                <ul v-for="(element, index) in secondLists" :key="index">
                    <h3>{{ element.title }}</h3>
                    <li v-for="(element, index) in element.elements">
                        <a href="element.link">{{ element.nome }} </a>
                    </li>
                </ul>
            </div>

        </div>

    </div>


</template>

<style scoped lang="scss">

    .big-container{
        background-image: url('/images/footer-bg.jpg');
        color: white;

        .container{
            display: flex;
            width: 80%;
            height: 100%;
            margin: auto;
            background-image: url('/images/dc-logo-bg.png');
            background-position: center right;
            background-repeat: no-repeat;
    
            .lists-1{
                ul{
                    margin-right: 1.5rem;
                    margin-top: 1.2rem;
                    padding-bottom: 1.2rem;
                }
            }
    
            .lists-2{
                display: flex;
    
                ul{
                    margin: 0 1.5rem;
                    margin-top: 1.2rem;
                }
            }
        }

    }

    h3{
        padding: 0.5rem 0;
    }

    li{
        margin: 0.3rem 0;
    }

    a{
        color: rgba($color: #ffffff, $alpha: 0.5);
        font-size: 0.8rem;
    }

</style>