<template>
  <!-- <PostsList /> -->
  <!-- <TemplateRef /> -->
  <ClickCounter />
</template>

<script>
// import PostsList from './components/PostsList.vue'
// import TemplateRef from './components/TemplateRef.vue'
import ClickCounter from './components/ClickCounter.vue'

export default {
  name: "App",
  components:{
    //  PostsList, 
    // TemplateRef,
    ClickCounter,
  },
  data() {
    return {
      
    };
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
