<template>
  <div class="nero">
    <div>
      <LogoComp />
    </div>



    <div>
      <ParteAlbum />
      <CardAlbum />
    </div>


  </div>

</template>



<script>
  import "bootstrap"
  import LogoComp from './components/LogoComp.vue'
  import ParteAlbum from './components/ParteAlbum.vue'
  import CardAlbum from './components/CardAlbum.vue'


  export default {
    name: 'App',
    components: {
      LogoComp,
      ParteAlbum,
      CardAlbum
    }

  }
</script>



<style lang="scss">
  @import "bootstrap/dist/css/bootstrap.min.css";

  .nero {
    background-color: red;
    
  }
</style>