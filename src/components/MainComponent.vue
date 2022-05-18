<template>

  <main>

    <HeaderComponent @search="selectedGenre" />
  
    <div class="container" v-if="loadingPage">

      <CardAlbum  v-for="(album, index) in filteredAlbum"
                  :key="`album${index}`"
                  :albumData="album"
      />
    </div>

    <div v-else>

      <div class="middle">
        <div class="bar bar1"></div>
        <div class="bar bar2"></div>
        <div class="bar bar3"></div>
        <div class="bar bar4"></div>
        <div class="bar bar5"></div>
        <div class="bar bar6"></div>  
        <div class="bar bar7"></div>
        <div class="bar bar8"></div>
      </div>

    </div>
  </main>
  
</template>

<script>

import CardAlbum from './CardAlbum.vue';
import HeaderComponent from './HeaderComponent.vue';
import axios from 'axios';

export default {
    name: 'MainComponents',
    components: { CardAlbum, HeaderComponent },

    data() {
      return{
        apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music', 
        dataAlbum: [],
        loadingPage: false,
        albumForSearch: ''     
    }
  },

  methods: {
    GetApi() {
      axios.get(this.apiUrl)

      .then(res => {
        // console.log(res.data);
        this.dataAlbum = res.data.response;
        this.loadingPage = true;
      })

      // .catch(err =>{
      //   console.log(err);
      // })

    },

    selectedGenre(genreAlbum) {
      console.log(genreAlbum);
      this.albumForSearch = genreAlbum
    }
  },

  computed: {
    filteredAlbum() {
      let arrayFiltered = [];
      
      if(this.albumForSearch === 'all'){
        arrayFiltered = this.dataAlbum;
      }
      else {
        arrayFiltered = this.dataAlbum.filter(album =>{
          return album.genre.includes(this.albumForSearch)
        })
      }

      return arrayFiltered
    }
  },
  
  mounted() {
    this.GetApi();
  }
}

</script>

<style lang="scss" scoped>

  @import '../assets/style/vars';

  main {
    background-color: #1E2D3B;
    height: 100vh;
  }

  .container {
    display: flex;
    flex-wrap: wrap;
  }

  .middle {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  position: absolute;
  }

  .bar {
    width: 10px;
    height: 70px;
    background: #fff;
    display: inline-block;
    transform-origin: bottom center;
    border-top-right-radius: 20px;
    border-top-left-radius: 20px;
    /*   box-shadow:5px 10px 20px inset rgba(255,23,25.2); */
    animation: loader 1.2s linear infinite;
  }

  .bar1 {
    animation-delay: 0.1s;
  }

  .bar2 {
    animation-delay: 0.2s;
  }

  .bar3 {
    animation-delay: 0.3s;
  }

  .bar4 {
    animation-delay: 0.4s;
  }

  .bar5 {
    animation-delay: 0.5s;
  }

  .bar6 {
    animation-delay: 0.6s;
  }

  .bar7 {
    animation-delay: 0.7s;
  }

  .bar8 {
    animation-delay: 0.8s;
  }

  @keyframes loader {
    0% {
      transform: scaleY(0.1);
      background: transparent;
    }
    50% {
      transform: scaleY(1);
      background: #34BE58
    }
    100% {
      transform: scaleY(0.1);
      background: transparent;
    }
}

</style>