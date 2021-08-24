<template>
  <h1>Hello {{ name }}</h1>
  <h1 v-text="name"></h1>
  <div v-html="html"></div>
  <button :disabled="isDisabled">Dsiabled</button>
  <h4 class="underline" :class="status">Status</h4>
  <h4 :class=" isStriked ? 'slant': 'normal' ">Green and slant </h4>
  <h4 :class=" [isStriked ? 'slant': 'normal', isGreen && 'green'] ">Green and slant array</h4>
  <h4 :class="{
    'slant':isStriked,
    'green':isGreen,
    
  }">Green and slant object
  </h4>
  <h4 :style="styleObj">Style binding using object</h4>
  <h4 :style="[ styleObj , styleObj2 ]">Style binding using array</h4>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      name:'Abobo',
      html:`<h1> Abobo HTML </h1>`,
      isDisabled: false,
      status:'danger',
      isStriked:false,
      isGreen: true,
      styleObj:{
        color:'yellow',
        fontWeight:'bold'
      },
      styleObj2:{
        backgroundColor:'green',
        padding: 4 + 'px'
      }
    };
  },
}
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
.underline{
  text-decoration: underline;
}

.danger{
  color: red;
}

.slant{
  text-decoration: line-through;
}

.green{
  color: green;
}
</style>
