<template>
  <div id="app">
    <Header v-bind:artist="artist" v-bind:logo="logoUrl"/>
    <SongOfTheDay v-bind:data="songs"/>
  </div>
</template>

<script>
import Header from './components/Header'
import SongOfTheDay from './components/SongOfTheDay'
import btsData from './data/bts-songs.js'

export default {
  name: 'App',
  components: {
    Header,
    SongOfTheDay
  },
  computed: {
    logoUrl() {
      return btsData.logoUrl
    },
    artist() {
      return btsData.artist
    },
    songs() {
      return btsData.songs
    }
  }
}
</script>

<style>
body {
  background-color: #966FD6;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
