<template>
  <div id="app">
    <h1>Basics of Vue.js</h1>
    <router-view/>
    <footer><img src="./assets/Labtic.png" alt="LabTIC" class="logo"></footer>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.logo{
  width: 150px;
  position: fixed;
  bottom: 1%;
  left: 45%;
  margin: 15px;
  padding: 5px;
  border:1px solid black ;
}
</style>
