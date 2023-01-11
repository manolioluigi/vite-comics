<script>

    export default {
        name: "AppMain",
        data(){
            return{
                
            }
        }

    }

</script>

<template>
    
  <div class="container-main">

    <div class="row">

        <div class="col">

            Content

        </div>

    </div>

  </div>

</template>

<style lang="scss">
    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .container-main{
        width: 100%;
        text-align: center;
        height: 100%;
        background-color: red;
    }

</style>