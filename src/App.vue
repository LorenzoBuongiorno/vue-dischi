<template>
  <div id="app">
    <header></header>
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

</style>
