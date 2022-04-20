<template>
  <div class="row">
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
          console.log(res.data);
          this.AlbumArray = res.data
        })

        .catch((error) => {
          console.log(error)
        })
    }

  }
</script>

<style scoped lang="scss">


</style>