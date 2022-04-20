<template>
  <div class="row row-cols-5 massimo">
    <!--Questo è il componente figlio a cui passare i dati-->
    <CardAlbum v-for="( element, index ) in AlbumArray" :key="index" :poster="element.poster" :title="element.title"
      :author="element.author" :year="element.year" />

  </div>
</template>

<script>
  import axios from 'axios';
  import CardAlbum from './CardAlbum.vue'

  export default {

    name: 'ParteAlbum',
    components: {
      CardAlbum
    },
    data() {
      return {
        AlbumArray: []
      }
    },
    created() {
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((res) => {
          console.log(res.data.response);
          this.AlbumArray = res.data.response
        })

        .catch((error) => {
          console.log(error)
        })
    }

  }
</script>

<style scoped lang="scss">
.massimo{
  max-width: 100%;
}

</style>