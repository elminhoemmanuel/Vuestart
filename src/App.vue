<template>
  <h2>Hello</h2>
  <h2>{{ add( 2, 4 , 6) }}</h2>
  <h2>{{ multiply( 6 ) }}</h2>
  
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      multiplier: 10
    };
  },
  methods : {
    add (a, b, c){
      return a + b + c
    },
    multiply ( num ){
      return num * this.multiplier
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
</style>
