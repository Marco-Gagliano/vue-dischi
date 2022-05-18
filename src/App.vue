<template>

  <div id="app">
    
    <MainComponent/>
    
  </div>
  
</template>

<script>

import MainComponent from './components/MainComponent.vue'

export default {
  name: 'App',
  components: {
    MainComponent
  }
}

</script>

<style lang="scss">

  @import './assets/style/vars';
  @import './assets/style/general';
  @import './assets/style/utils';
  @import './assets/style/mixins';

</style>
