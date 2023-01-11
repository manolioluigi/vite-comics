<script>

    export default {
        
        name: "AppFooter",
        data(){
            return{
                
                menu: [
                    {
                        label: 'DIGITAL COMICS',
                        url: '#',
                        image: '../assets/img/buy-comics-digital-comics.png'
                    },
                    {
                        label: 'DC MERCHANDISE',
                        url: '#',
                        image: '../assets/img/buy-comics-merchandise.png'
                    },
                    {
                        label: 'SUBSCRIPTION',
                        url: '#',
                        image: '../assets/img/buy-comics-subscriptions.png'
                    },
                    {
                        label: 'COMIC SHOP LOCATOR',
                        url: '#',
                        image: '../assets/img/buy-comics-shop-locator.png'
                    },
                    {
                        label: 'DC POWER VISA',
                        url: '#',
                        image: '../assets/img/buy-dc-power-visa.svg'
                    }
                ],

                comics: [
                    {
                        label: 'Characters'
                    },
                    {
                        label: 'Comics'
                    },
                    {
                        label: 'Movies'
                    },
                    {
                        label: 'TV'
                    },
                    {
                        label: 'Games'
                    },
                    {
                        label: 'Videos'
                    },
                    {
                        label: 'News'
                    }
                ],

                shop: [
                    {
                        label: 'Shop DC'
                    },
                    {
                        label: 'Shop DC Collectibles'
                    }
                ],

                dc: [
                    {
                        label: 'Terms Of Use'
                    },
                    {
                        label: 'Privacy policy (New)'
                    },
                    {
                        label: 'Ad Choices'
                    },
                    {
                        label: 'Advertising'
                    },
                    {
                        label: 'Jobs'
                    },
                    {
                        label: 'Subscriptions'
                    },
                    {
                        label: 'Talent Workshops'
                    },
                    {
                        label: 'CPSC Certificates'
                    },
                    {
                        label: 'Ratings'
                    },
                    {
                        label: 'Shop Help'
                    },
                    {
                        label: 'Contact Us'
                    }
                ],

                sites: [
                    {
                        label: 'DC'
                    },
                    {
                        label: 'MAD Magazine'
                    },
                    {
                        label: 'DC Kids'
                    },
                    {
                        label: 'DC Universe'
                    },
                    {
                        label: 'DC Power Visa'
                    }
                ]

            }
        }

    }

</script>

<template>
    
    <div>

        <div class="container-footer">

            <div class="row bg-blue">

                <div v-for="(item, index) in menu" :key="index" class="col">
                    
                    <div class="col-width-15">
                        <img :src="item.image" alt="">
                        <span class="margin-left-10">{{item.label}}</span>
                    </div>

                </div>

            </div>

            <div class="row bg-image">

                <div class="col col-12">

                    <h3>DC COMICS</h3>

                    <ul>

                        <li v-for="(item, index) in comics" :key="index">
                            <a href="#">{{ item.label }}</a> 
                        </li>

                    </ul>

                    <h3>SHOP</h3>

                    <ul>

                        <li v-for="(item, index) in shop" :key="index">
                            <a href="#">{{ item.label }}</a> 
                        </li>

                    </ul>

                </div>
                <div class="col col-12">

                    <h3>DC</h3>

                    <ul>

                        <li v-for="(item, index) in dc" :key="index">
                            <a href="#">{{ item.label }}</a> 
                        </li>

                    </ul>

                </div>
                <div class="col col-12 margin-bottom-140">

                    <h3>SITES</h3>

                    <ul>

                        <li v-for="(item, index) in sites" :key="index">
                            <a href="#">{{ item.label }}</a> 
                        </li>

                    </ul>

                </div>
                <div class="col col-logo">
                    <img src="/assets/img/dc-logo-bg.png" alt="logo">
                </div>
                
            </div>

            <div class="row bg-dark-gray between">

                <div class="col">

                    <div class="button">

                        <span>SIGN-UP NOW!</span>

                    </div>

                </div>

                <div class="col">

                    <div class="social">

                        <span>FOLLOW US</span>
                        <img src="/assets/img/footer-facebook.png" alt="">
                        <img src="/assets/img/footer-twitter.png" alt="">
                        <img src="/assets/img/footer-youtube.png" alt="">
                        <img src="/assets/img/footer-pinterest.png" alt="">
                        <img src="/assets/img/footer-periscope.png" alt="">
                    
                    </div>

                </div>

            </div>

        </div>

    </div>

</template>

<style lang="scss">
    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .container-footer{
        width: 100%;
        text-align: center;
        height: 100%;
        position: relative;

        .between{
            justify-content: space-between;
            padding-left: 10vw;
            padding-right: 10vw;
        }
    }

    .col-width-15{
        width: 15vw;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 12px;
        color: white;

        img{
            height: 40px;
        }

    }

    .col-12{
        width: 12vw;
        text-align: left;
    }

    .col-logo{
        display: flex;

        img{
            width: 80%;
            align-self: end;
        }
    }

    .bg-blue{
        background-color: $blue;
        padding: 40px 0 40px 0;
        position: absolute;
        top: 0;
    }

    .bg-image{
        background-image: url(/assets/img/footer-bg.jpg);
        padding: 40px 0 40px 0;

        h3{
            color: $white;
            margin-top: 20px;
        }
        
    }

    .bg-dark-gray{
        background-color: $darkgray;
        padding: 25px 0 25px 0;
        position: absolute;
        bottom: 0;
        
    }

    .margin-left-10{
        margin-left: 10px;
    }

    .margin-bottom-140{
        margin-bottom: 140px;
    }

    .col-12{

        ul {
        
            display: flex;
            flex-direction: column;
            line-height: 0.2;

            a{
                color: $gray;
                text-decoration: none;
            }
        }

        li {
            margin: 10px 0 10px 0;
            font-size: 12px;
        }
    }

    .button{
        padding: 5px 10px 5px 10px;
        color: $white;
        border: 2px solid $blue;
        font-size: 15px;
    }

    .social{
        display: flex;
        justify-content: center;
        align-items: center;
        color: $blue;

        span{
            margin-right: 10px;
        }
        img{
            margin: 0 10px;
        }
    }

</style>