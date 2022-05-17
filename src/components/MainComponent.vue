<template>

  <main>
    <div class="container ">

      <CardAlbum/>
      <CardAlbum/>
      <CardAlbum/>
      <CardAlbum/>
      <CardAlbum/>
      <CardAlbum/>
      <CardAlbum/>
      <CardAlbum/>
      
    </div>
  </main>
  
</template>

<script>
import CardAlbum from './CardAlbum.vue';

export default {
    name: 'MainComponents',
    components: { CardAlbum }
}

</script>

<style lang="scss" scoped>

  @import '../assets/style/vars';

  main {
    background-color: #1E2D3B;
    padding-top: 55px;
  }

  .container {
    display: flex;
    flex-wrap: wrap;
  }

</style>