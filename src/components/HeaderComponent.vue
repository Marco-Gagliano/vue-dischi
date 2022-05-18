<template>
  
  <header>
    <div class="container-fluid">
      <div class="banner">

        <a href="#">
          <img src="../assets/img/logo-small.svg" alt="">
        </a>

        <SelectGenre/>
        

      </div>
    </div>
  </header>

</template>

<script>

import SelectGenre from './SelectGenre.vue';

export default {
  name: 'HeaderComponent',

  components: { SelectGenre }
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

  img  {
    width: 50px;
  }
</style>