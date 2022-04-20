<template>
  <div>
    <LogoComp/>
    <ParteAlbum/> 
  </div>

</template>



<script>
  import "bootstrap"
  import LogoComp from './components/LogoComp.vue'
  import ParteAlbum from './components/ParteAlbum.vue'


  export default {
    name: 'App',
    components: {
      LogoComp,
      ParteAlbum,
    }

  }
</script>



<style lang="scss">
  @import "bootstrap/dist/css/bootstrap.min.css";
</style>