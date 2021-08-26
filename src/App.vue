<template>
  <!-- <h2>Hello</h2>
  <h2>{{ add( 2, 4 , 6) }}</h2>
  <h2>{{ multiply( 6 ) }}</h2> -->
  <!-- <p>{{name}}</p>
  <button v-on:mouseout="name = 'Abobo'">click</button> -->

  <!-- <div>
    <h3>{{count}}</h3>
    <button v-on:click="increase(5)">Increase</button>
    <button v-on:click="decrease(5)">Decrease</button>
  </div> -->
  <div>
    <h3>{{count}}</h3>
    <button @click="increase(5, $event)">Increase</button>
    <button @click="decrease(5)">Decrease</button>
  </div>
  
  
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      multiplier: 10,
      name:'omale',
      count: 0,
    };
  },
  methods : {
    // add (a, b, c){
    //   return a + b + c
    // },
    // multiply ( num ){
    //   return num * this.multiplier
    // }
    increase(num, event){
      this.count += num,
      console.log("event was", event)
    },
    decrease(num){
      this.count -= num
    },
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
