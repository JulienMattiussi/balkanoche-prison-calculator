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
}

.content {
  position: relative;
  margin-top: 150px;
  overflow:hidden;
  background-size: cover;
  background-position: top;
  background-clip: content-box;
  background-image:url(assets/open-fence_light.jpg);
  height: calc(100vh - 200px);
}

@media (max-width: 1250px) {
    .content {
        margin-top: 110px;
        font-size: 12px;
        line-height: 25px;
        background-size: contains;
        height: 100%;
    }
}
</style>
