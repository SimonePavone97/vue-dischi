<template>
    <div class="col text-center my-5">
        <img :src="poster" alt="">
        <h3 class="my-3">{{title}}</h3>
        <h4 class="my-3">{{author}}</h4>
        <span class="fw-bolder my-3">{{year}}</span>
    </div>
</template>

<script>
    export default {

        name: 'CardAlbum',

        props: {
            poster: String,
            title: String,
            author: String,
            year: String,
        }
    }
</script>

<style scoped lang="scss">


img{
    height: 200px;
}


</style>