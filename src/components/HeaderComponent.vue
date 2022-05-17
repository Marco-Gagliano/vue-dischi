<template>
  
  <header>
    <div class="container-fluid">
      <div class="banner">

        <a href="#">
          <img src="../assets/img/logo-small.svg" alt="">
        </a>

        <select class="form-select" aria-label="Default select example">
          <option selected>Seleziona un genere</option>
          <option value="metal">Metal</option>
          <option value="rock">Rock</option>
          <option value="pop">Pop</option>
          <option value="jazz">Jazz</option>
        </select>

      </div>
    </div>
  </header>

</template>

<script>
export default {
  name: 'HeaderComponent'
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