<script>

    export default {
        name: "AppHeader",
        data(){
            return{
                logo: '../assets/img/dc-logo.png',
            }
        }

    }

</script>

<template>
  
    <header>

        <div class="container-header">

            <div class="row">

                <div class="col">

                    <img :src="logo" alt="logo">

                </div>

                <div class="col">

                    

                </div>

            </div>

        </div>

    </header>

</template>

<style>

</style>