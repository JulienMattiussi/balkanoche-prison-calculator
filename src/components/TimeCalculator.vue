<template>
  <div class="main">
    <div class="data">
      <h1>Découvrez combien vous risquez en appliquant la jurisprudence Balkanoche 2019-2022</h1>
      <h1>Si vous avez commis :</h1>
        <select v-model="crime">
            <option value="13000000">Le détournement de 13 millions d'euros</option>
            <option value="30000">Un cambriolage dans un quartier riche</option>
            <option value="100000">Une douzaine de cambriolages divers</option>
            <option value="20000">Le vol d'une voiture neuve</option>
            <option value="50000">50 vols de voitures</option>
            <option value="20">Un petit vol dans un magasin</option>
            <option value="10">Un stationnement sans payer</option>
        </select>
      <h1>Vous risquez de passer :</h1>
      <CountDown :crime="crime" />
    </div>
  </div>
</template>

<script>
import CountDown from "./CountDown.vue";

export default {
  name: "TimeCalculator",
  components: {
    CountDown,
  },
  data() {
     return {
        crime: "13000000",
    };
},
  methods: {
    changeCrime(value) {
      this.crime = value;
    },
  },
};
</script>

<style scoped>
.main {
  display: flex;
  justify-content: center;
  width: 100%;
  margin: 10px 0 0;
}

.data {
  display: flex;
  flex-direction: column;
  align-items: baseline;
  width: 800px;
}

select {
    font-size: 30px;
    width: 650px;
};

@media (max-width: 1250px) {
  .numbers {
    font-size: 40px;
  }
}
</style>
