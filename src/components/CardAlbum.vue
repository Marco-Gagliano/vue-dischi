<template>

  
  <div class="album">

    <div>
      <img src="https://upload.wikimedia.org/wikipedia/en/1/1d/Slipknot_Iowa.jpg" alt="">
    </div>

    <h5>Iowa</h5>
    <span>Slipknot</span>
    <span>2001</span>

  </div>
  

</template>

<script>


export default {
  name: 'CardAlbum'

  

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