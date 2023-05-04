<script>

    export default{
        name: 'AppComics',
        props: ['singleComic']
    }

</script>

<template>

    <div class="card">
        <img :src="singleComic.thumb" alt="comics">
        <p>{{ singleComic.series }} </p>
    </div>
    
</template>

<style scoped lang="scss">

    .card{
        width: calc(100% / 6 - 1rem);
        margin-bottom: 2rem;

        img{
           width: 100%;
           height: 9rem;
           object-fit: cover;
           object-position: top;
        }

        p{
            text-transform: uppercase;
            color: rgba($color: #ffffff, $alpha: 0.8);
            font-size: 0.7rem;
            margin-top: 5px;
        }
    }

</style>