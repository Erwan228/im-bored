<template>
  <div id="divflex">
    <div id="pink" class="eyes"></div><div id="yello" class="eyes"></div>
  </div>
  <p @click="trappedClick">HEY EVERY !! IT'S ME!!! EV3RY BUDDY 'S FAVORITE [[Number 1 Rated Salesman1997]] SPAMT SPAMTON G. SPAMTON!!</p>
  <salesPitch v-if="salesPitchShow" @click="showDealLMA0">
    <template v-slot:salesPitch1>
      <p>DO YOU WANNA HEAR ABOUT THE [[0.99$ Deal]] YOU CAN MAKE WITH ME?<br>
      BECAUSE I KNOW. EXCACTLY. WHAT YOU. WANT!!!!1!</p>
    </template>
  </salesPitch>
  <br>
  <salesPitch v-if="showPitch2" @click="showTheProduct$$$$">
    <template v-slot:salesPitch2>
      <p>AND. THAT. IS ..</p>
    </template>
  </salesPitch>
  
</template>

<script>
import salesPitch from './components/salesPitch.vue';
export default {
  name: 'App',
  data() {
    return {
      salesPitchShow: false,
      showPitch2: false,
    }
  },
  components: {
    salesPitch,
  },
  methods: {
    trappedClick(){
      this.salesPitchShow = true
    },
    showDealLMA0(){
      this.showPitch2 = true
    }
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
