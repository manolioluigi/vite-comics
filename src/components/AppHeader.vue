<script>

    export default {
        name: "AppHeader",
        data(){
            return{
                logo: '../assets/img/dc-logo.png',
                menu: [
                    {
                        label:'CHARACTERS',
                        url:'#',
                        active: false
                    },
                    {
                        label:'COMICS',
                        url:'#',
                        active: true
                    },
                    {
                        label:'MOVIES',
                        url:'#',
                        active: false
                    },
                    {
                        label:'TV',
                        url:'#',
                        active: false
                    },
                    {
                        label:'GAMES',
                        url:'#',
                        active: false
                    },
                    {
                        label:'COLLECTIBLES',
                        url:'#',
                        active: false
                    },
                    {
                        label:'VIDEOS',
                        url:'#',
                        active: false
                    },
                    {
                        label:'FANS',
                        url:'#',
                        active: false
                    },
                    {
                        label:'NEWS',
                        url:'#',
                        active: false
                    },
                    {
                        label:'SHOP',
                        url:'#',
                        active: false
                    }
                
                ]
            }
        }

    }

</script>

<template>
  
    <header>

        <div class="container-header">

            <div class="row between">

                <div class="col">

                    <img :src="logo" alt="logo" class="logo">

                </div>

                <div class="col col-menu">

                    <nav>

                        <ul>

                            <li v-for="(item, index) in menu" :key="index">
                                <a href="item.url" :class="item.active ? 'active' :''"></a>
                                {{ item.label }}
                            </li>

                        </ul>

                    </nav>

                </div>

            </div>

        </div>

    </header>

</template>

<style lang="scss">

    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .container-header{
        width: 100%;
        height: 100%;
        text-align: center;
    }

    .row{
        @include center;
    }

    .col-menu{
        width: 70%;
        padding-right: 10vw;
    }

    .between{
        justify-content: space-between;
    }

    ul{
        @include center;
    }

    li{
        display: inline-block;
        margin: 10px;
        font-size: 12px;
    }

    .active{
        color: $blue;
    }

    .logo{
        width: 70px;
        margin-left: 10vw;
        margin-top: 20px;
        margin-bottom: 20px;
    }


</style>