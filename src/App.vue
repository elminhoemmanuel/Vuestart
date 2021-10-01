<template>
    <!-- <Greet name="Abobo" />
    <Greet name="Omale" />
    <Greet name="Amodu" />
    <Greet :name="name" :job="job" />

    <Article id="my-article" title="My Life" :likes="50" :isPublished="false" /> -->

    <!-- <ComponentC /> -->
    <!-- <button @click="showPopup = true">Show Popup</button>
    <Popup v-show="showPopup" @close="closePopup" /> -->
    <Input v-model="name" />
</template>

<script>
import Greet from "./components/Greet.vue"
import Article from "./components/Article.vue"
import ComponentC from "./components/ComponentC.vue"
import Popup from "./components/Popup.vue"
import Input from "./components/Input.vue"

export default {
  name: "App",
  components:{
    Greet,
    Article,
    ComponentC,
    Popup,
    Input
  },
  data() {
    return {
      // name:"Omale",
      // job:"SDE",
      // showPopup: false,
      name:""
    };
  },
  methods: {
    closePopup(gotten){
      this.showPopup = false
      console.log("Got", gotten)
    }
  },
  computed: {},
  watch: {
    
  },
  provide(){
    return {
      username:"Omale"
    }
  }
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
