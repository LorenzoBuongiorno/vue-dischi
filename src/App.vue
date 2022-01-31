<template>
  <div id="app">
    <header>
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png" alt="">
    </header>
    <main-container :dischi="dischi" />
  </div>
</template>

<script>
import MainContainer from './components/MainContainer.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    MainContainer
  },
    data (){
    return {
      dischi: []
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((element) => {
      this.dischi = element.data.response
    })
  }
  

}
</script>

<style lang="scss">
header{
  height: 8vh;
  background-color: #2e3a46;
  padding: 10px;
  img{
    height: 100%;
  }
}
@import './style/main.scss';
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
</style>
