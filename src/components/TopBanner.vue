<template>
  <div class="banner">
    <img alt="Marmelab logo" src="../assets/prisonner.png" />
    <TitleMessage
      msg="Balkanoche Prison Calculator"
    />
    <img alt="Marmelab logo" src="../assets/free.png" />
  </div>
</template>

<script>
import TitleMessage from "./TitleMessage.vue";

export default {
  name: "TopBanner",
  components: {
    TitleMessage,
  },
};
</script>

<style scoped>
.banner {
    position: absolute;
    top: 0;
    width: 100%;
    height: 100px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    background-color : #FF8C00;
    border-bottom: solid black 4px;

}
</style>
