<template>
  <!-- <div>
    <h3 v-if="num === 0">the number is zero</h3>
    <h3 v-else-if="num < 0">the number is negative</h3>
    <h3 v-else-if="num > 0">the number is positive</h3>
    <h3 v-else>Not a number</h3>

    <template v-if="display"> I am a good guy </template>
    <h2 v-show="display">I am a good guy vshow</h2>
  </div> -->
  <div>
    <!-- <h3 v-for=" ( name , index) in names" :key="name">{{ index+1 }} {{ name }}</h3> -->
    <!-- <h3 v-for=" ( name , index) in fullNames" :key="name">{{ index+1 }} {{ name.first }} {{ name.last }}</h3> -->
    <!-- <div v-for=" ( role , index) in roles" :key="role">
      <h2>{{ index+1 }} {{role.title}}</h2>
      <h4 v-for=" job  in role.jobs" :key="job"> {{ job }} </h4>
    </div> -->

    <!-- <div v-for="(value, key) in me " :key="value">
      {{ key }} {{ value }}
    </div> -->

    <template v-for="name in names" :key="name">
      <h2 v-if="name === 'Omale'">{{name}}</h2>
    </template>
    
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      num: 5,
      display: true,
      names:['Omale', 'Christy', 'Victoria', 'David'],
      fullNames:[ {first:'Omale', last:"Amodu"}, 
      {first:'Victoria', last:"Amodu"},
      {first:'Christy', last:"Amodu"},
      ],
      roles:[
        {
          title:"Omale Amodu",
          jobs:["Developer", "Engineer"]

        },
        {
          title:"victoria Amodu",
          jobs:["Fashion Designer", "Event Planner"]

        },
        {
          title:"Christy Amodu",
          jobs:["Reporter", "Presenter"]

        }
      ],
      me:{
        name:"Emmanuel Amodu",
        job:'Developer'
      }
    };
  },
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
