<template>
  <div id="app">
    <header>
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png" alt="">
      <div class="select-menu">
        <select-genre @genre="filterGenre"/>
        <select-artist @artist="filterArtist"/>
      </div>
    </header>
    <loader class="loader" v-if="!loaded"/>
    <main-container v-else :dischi="artistFiltered" />
  </div>
</template>

<script>
import MainContainer from './components/MainContainer.vue'
import axios from 'axios'
import SelectGenre from './components/SelectGenre.vue'
import Loader from './components/Loader.vue'
import SelectArtist from './components/SelectArtist.vue'

export default {
  name: 'App',
  components: {
    MainContainer,
    Loader,
    SelectGenre,
    SelectArtist,
  },
    data (){
    return {
      dischi: [],
      dischiFiltered: [],
      artistFiltered: [],
      loaded: false
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((element) => {
      this.dischi = element.data.response
      this.dischiFiltered = element.data.response
      this.artistFiltered = element.data.response
      this.loaded = true;
    })
  },
  methods: {
    filterGenre(keywordSearch) {
      if (keywordSearch == 'All'){
        this.dischiFiltered = this.dischi.filter((disco) => {
          return disco.genre.includes('');
        })
      } else {
        this.dischiFiltered = this.dischi.filter((disco) => {
          return disco.genre.includes(keywordSearch);
        })
      }
      this.artistFiltered = this.dischiFiltered;
    },
  filterArtist(keywordSearchArtist) {
      if (keywordSearchArtist == 'All' || keywordSearchArtist == ''){
        this.artistFiltered = this.dischiFiltered.filter((disco) => {
          return disco.author.includes('');
        })
      } else {
        this.artistFiltered = this.dischiFiltered.filter((disco) => {
          return disco.author.includes(keywordSearchArtist);
        })
      }
    }
  }

  

}
</script>

<style lang="scss">
#app{
  position: relative;
  header{
    height: 70px;
    background-color: #2e3a46;
    padding: 10px;
    display: flex;
    img{
      height: 100%;
    }
    .select-menu{
      width: 100%;
      display: flex;
      justify-content: center
    }
  }
}
@import './style/main.scss';
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
</style>
