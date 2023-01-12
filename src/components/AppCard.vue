<script>
    export default {
        name: 'AppCard',
        props:{
            comic: Object
        }

    }
</script>

<template>

    <div class="card">
        <div class="card-image">
            <img :src="comic.thumb" alt="">
        </div>
        <div>
            <p class="title">{{ comic.series }}</p>
            <span>{{ comic.price }}</span>
            <span>{{ comic.type }}</span>
        </div>
    </div>

</template>

<style lang="scss" scoped>

    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .card{
        display: flex;
        flex-direction: column;
        color: $white;
        margin: 10px;
        height: 250px;
    }
    .card-image{
        img{
            width: 200px;
            height: 200px;
            object-fit: cover;
            object-position: 50% top;
        }
    }

    .title{
        font-weight: 50%;
        font-size: 18px;
        inline-size: 200px
    }

    span{
        font-size: 12px;
        margin: 0px 2px 0px 2px;
        font-style: italic;
    }

</style>