<template>
  <img class="back" alt="Fence" src="./assets/open-fence.jpg" /> <TopBanner />
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
  color: #2c3e50;
  padding-top: 0px;
}

@media (max-width: 1250px) {
  #app {
    padding-top: 10px;
  }
}

.back {
  width: 100%;
  margin: 0;
  position: absolute;
  z-index: 0;
  top: 0;
  left: 0;
  filter: contrast(40%) blur(5px) brightness(1.5);
}

@media (max-width: 1250px) {
  .back {
    margin: -10px;
    height: calc(100% + 20px);
    width: unset;
  }
}

.content {
  position: relative;
  margin-top: 150px;
}
</style>
