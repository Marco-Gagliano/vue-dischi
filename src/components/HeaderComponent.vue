<template>
  
  <header>
    <div class="container-fluid">
      <div class="banner">

        <a href="#">
          <img src="../assets/img/logo-small.svg" alt="">
        </a>

        <select v-model="albumGenre"
                @change="$emit('search', albumGenre)"
                class="form-select" 
                aria-label="Default select example">

          <option value="all">Seleziona un genere</option>
          <option value="Metal">Metal</option>
          <option value="Rock">Rock</option>
          <option value="Pop">Pop</option>
          <option value="Jazz">Jazz</option>
        </select>

      </div>
    </div>
  </header>

</template>

<script>

export default {
  name: 'HeaderComponent',

  data() {
    return{
      albumGenre: "all"
    }
  }
}

</script>

<style lang="scss" scoped>

  @import '../assets/style/vars';

  .container-fluid {
    background-color: #2E3A46;
    margin: 0;
  }

  .banner {
    display: flex;
    justify-content: space-between;
    padding: 22px
  }

  select {
    padding: 5px 20px;
    font-size: 18px;
    background-color: #000000;
    color: #34BE58;
  } 
    
  .form-select {
    width: 16%
  }

  img  {
    width: 50px;
  }
  
</style>