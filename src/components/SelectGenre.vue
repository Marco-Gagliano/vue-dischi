<template>
  
  <select class="form-select" aria-label="Default select example">
    <option selected>Seleziona un genere</option>
    <option value="metal">Metal</option>
    <option value="rock">Rock</option>
    <option value="pop">Pop</option>
    <option value="jazz">Jazz</option>
  </select>

</template>

<script>
export default {
  name: 'SelectGenre'

}
</script>

<style lang="scss" scoped>

  select {
    padding: 5px 20px;
    font-size: 18px;
    background-color: #000000;
    color: #34BE58;
  } 
    
  .form-select {
    width: 16%
  }

</style>