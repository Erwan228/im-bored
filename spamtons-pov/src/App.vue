<template>
  <div id="divflex">
    <div id="pink" class="eyes"></div><div id="yello" class="eyes"></div>
  </div>
  <p @click="trappedClick" v-if="showIntro">HEY EVERY !! IT'S ME!!! EV3RY BUDDY 'S FAVORITE [[Number 1 Rated Salesman1997]] SPAMT SPAMTON G. SPAMTON!!</p>
  <salesPitch v-if="salesPitchShow" @showNext1="showDealLMA0">
    <template v-slot:salesPitch1>
      <p>DO YOU WANNA HEAR ABOUT THE [[0.99$ Deal]] YOU CAN MAKE WITH ME?</p>
    </template>
  </salesPitch>
  <salesPitch v-if="showPitch2" @showNext2="showPitcher3">
    <template v-slot:salesPitch2>
  <p>BECAUSE I KNOW. EXCACTLY. WHAT YOU. WANT!!!</p>
    </template>
  </salesPitch>
  <salesPitch v-if="showPitch3" @showNext3="showTheProduct$$$$">
    <template v-slot:salesPitch3>
      <p>AND. THAT. IS ..</p>
    </template>
  </salesPitch>
  <Deal v-if="sh">
    <template v-slot: dealPart1>
      <button disabled>Choices</button>
    </template>
  </Deal>
</template>

<script>
import salesPitch from './components/salesPitch.vue';
import Deal from './components/deal.vue';
export default {
  name: 'App',
  data() {
    return {
      showIntro: true,
      salesPitchShow: false,
      showPitch2: false,
      showPitch3: false,
      revealDeal1: false,
    }
  },
  components: {
    salesPitch,
    Deal,
  },
  methods: {
    trappedClick(){
      this.salesPitchShow = true
      console.log(this.salesPitchShow)
    },
    showDealLMA0(){
      this.showPitch2 = true
      console.log(this.showPitch2)
    },
    showPitcher3(){
      this.showPitch3 = true
      console.log(this.showPitch3)
    },
    showTheProduct$$$$(){
      this.showIntro = false
      this.showPitch2 = false
      this.showPitch3 = false
      this.salesPitchShow = false
      this.revealDeal1 = true
    }

  }

}
</script>

<style>
*{
  user-select: none;
}
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
