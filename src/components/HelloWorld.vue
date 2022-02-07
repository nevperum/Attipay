<template>
  <div class="topbar">
    <img alt="Vue logo" src="../assets/logo.svg">
    
    <h2>{{ msg }}</h2>
    <h2>{{currentDate}}</h2>
      <my-component v-if="renderComponent" />
  </div>
  
  
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    currentDate: Date
    
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.topbar {
    background-color:rgb(24, 102, 69);
    width:100%;
    height:50px;
}
* {
  margin:0px;
  padding:0px;
}
img
{
   font-size: 21px;
   left: 738.994px;
}
h2
{
 color: rgb(255, 255, 255);
 display: inline;
 font-size: 21px;
 font-family: sans-serif;
 
}
Date
{
  left: 738.994px;
  top: 16.4248px;
  font-size: 13.4078px;
  font-family: sans-serif; 
  transform: scaleX(0.731502);
}
h3 {
  margin: 40px 0 0;
 
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
