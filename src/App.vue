<template>
  <h2>Volume Tracker (0-20)</h2>
  <h3>Current Volume - {{ volume }}</h3>

  <div>
    <button @click="volume += 1">Increase</button>
  </div>
  <div>
    <button @click="volume -= 1">Decrease</button>
  </div>

  <input type="text" v-model="movie" />
  <input type="text" v-model="movieInfo.title" />
  <input type="text" v-model="movieInfo.actor" />

  <button @click="movies.push('Supergirl')">Add Movie</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      volume: 0,
      movie: "",
      movieInfo:{
        title: "",
        actor: "",
      },
      movies:["Batman", "Superman"]
    };
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 10) {
        alert("Its not good to listen to loud music");
      }
    },
    movie: {
      handler(newValue) {
        console.log(`Calling API with movie name - ${newValue}`);
      },
      immediate: true
    },
    movieInfo: {
      handler(newValue) {
        console.log(`Calling API with movie name - ${newValue.title} and ${newValue.actor}`);
      },
      immediate: true,
      deep:true
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 20px;
}
</style>
