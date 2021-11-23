<template>
  <div class="random">
    <h2>{{ randomSong.title }}</h2>
    <iframe width="560" height="315" 
        v-bind:src="youtubeBaseUrl + randomSong.youtube"
        title="YouTube video player" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
    </iframe>
  </div>
</template>

<script>
export default {
  name: 'SongOfTheDay',
  data() {
    return {
      youtubeBaseUrl: 'https://www.youtube.com/embed/'
    }
  },
  computed: {
    randomSong() {
      let randomIndex = Math.floor( Math.random() * this.data.length )
      return this.data[randomIndex]
    }
  },
  props: {
    data: {
      type: [],
      required: true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.random {
  text-align: center;
}
</style>
