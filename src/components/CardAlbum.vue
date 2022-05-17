<template>

  
  <div class="album">

    <div>
      <img :src="albumData.poster" alt="">
    </div>

    <h5>{{albumData.title}}</h5>
    <span>{{albumData.author}}</span>
    <span>{{albumData.year}}</span>

  </div>
  

</template>

<script>




export default {
  name: 'CardAlbum',

  props: {
    albumData: Object
  } 
}

</script>

<style lang="scss" scoped>

  .album {
    flex-basis: calc(100% / 8);
    padding: 10px 10px 50px 10px;
    margin: 10px 10px;
    background-color: #2E3A46;
  }

  img {
    width: 150px;
    height: 150px;
  }

  h5, span {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  h5 {
    color: #FFFFFF;
    padding: 10px 0;
  }

  span {
    color: #7C7876;
  }

</style>