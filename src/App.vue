<template>
  <TopBanner />
  <div class="content">
    <TimeCalculator />
  </div>
  <BottomBanner />
</template>

<script>
import TopBanner from "./components/TopBanner.vue";
import BottomBanner from "./components/BottomBanner.vue";
import TimeCalculator from "./components/TimeCalculator.vue";

export default {
  name: "App",
  components: {
    TopBanner,
    BottomBanner,
    TimeCalculator,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  padding-top: 0px;
  overflow: hidden;
  background-size: 100%;
  height: 100vh;
}

@media (max-width: 1250px) {
  #app {
    height: auto;
  }
}

.back {
  width: 100%;
  margin: 0;
  position: absolute;
  z-index: 0;
  top: 0;
  left: 0;
  //filter: contrast(10%) blur(1px) brightness(2);
}

.content {
  position: relative;
  margin-top: 150px;
  overflow:hidden;
}

@media (max-width: 1250px) {
    .content {
        margin-top: 110px;
        font-size: 12px;
        line-height: 25px;
    }
}
</style>
