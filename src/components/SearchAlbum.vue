<template>

  <div class="container d-flex justify-content-center">
    <div>

      <input  v-model.trim="albumToSearch"
              @keyup.enter="$emit('albumSearch'), albumToSearch" type="text" placeholder="Ricerca">
    </div>

    <div>
      <button class="btn-search" @click="startSearch">Cerca</button>
    </div>


    <div>
      <button class="btn-reset" @click="startReset">Reset</button>
    </div>

  </div>
   
</template>

<script>
export default {
  name: 'SearchAlbum',

  data() {
    return {
      albumToSearch: ''
    }
  },

  methods: {
    sendSearch() {
      this.$emit('startSearch'), this.albumToSearch;
      this.textToSearch = '';
    },

    startReset() {
      this.textToSearch = '';
      this.$emit('startSearch'), this.albumToSearch;
    },
  }
}
</script>

<style lang="scss" scoped>

  input {
    border-radius: 10px;
    border: 0px;
    margin: 0 20px ;
  }

  .btn-search {
    margin: 0 10px ;
    background-color: #34BE58;
  }
  .btn-reset {
    background-color: #FF0000;
  }

</style>