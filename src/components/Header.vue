<template>
  <header>
    <h1>Song of the Day</h1>
    <img v-bind:alt="artist + ' logo'" v-bind:src="logo">
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    artist: {
      type: String,
      required: true
    }, 
    logo: {
      type: String,
      required: true
    }
  }
}
</script>

<style>
header {
  text-align: center;
  margin-bottom: 2rem;
  padding: 1rem;
}

header h1 {
  margin: 0 0 1rem 0;
}

header img {
  height: 7rem;
}
</style>