<template>
  <div id="divflex">
    <div id="pink" class="eyes"></div><div id="yello" class="eyes"></div>
  </div>
  <p>HEY EVERY !! IT'S ME!!! EV3RY BUDDY 'S FAVORITE [[Number 1 Rated Salesman1997]] SPAMT SPAMTON G. SPAMTON!!</p>

</template>

<script>
import salesPitch from './components/salesPitch.vue';
export default {
  name: 'App',
  components: {
    salesPitch,
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#divflex{
  display:flex;
  justify-content: space-evenly;
}
.eyes{
  height: 404px;
  width: 404px;
}
#pink{
  background-color: pink;
}
#yello{
  background-color: yellow;
}
</style>
