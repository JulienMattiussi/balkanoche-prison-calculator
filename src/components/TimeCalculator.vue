<template>
  <div class="container">
    <div class="contained">
      <h1>Calculez la durée de votre peine de prison grâce à la jurisprudence Balkanoche 2019-2022</h1>
      <h1>Délit commis :</h1>
        <select class="selector" v-model="crime">
            <option value="13000000">Le détournement de 13 millions d'euros</option>
            <option value="30000">Un cambriolage dans un quartier riche</option>
            <option value="100000">Une douzaine de cambriolages divers</option>
            <option value="20000">Le vol d'une voiture neuve</option>
            <option value="50000">50 vols de voitures</option>
            <option value="20">Un petit vol dans un magasin</option>
            <option value="10">Un stationnement sans payer</option>
        </select>
      <h3>(Soit un vol estimé d'une valeur d'environ {{ crime }} € )</h3>
      <h1>Peine à exécuter :</h1>
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
.container {
  display: flex;
  justify-content: center;
  width: calc(100% - 20px);
  margin: 0 10px;
}

.contained {
  display: flex;
  flex-direction: column;
  align-items: baseline;
  width: 800px;
}

@media (max-width: 1250px) {
    .contained {
        width: 100%;
    }
}

@media (max-width: 1250px) {
    .selector {
        font-size: 15px !important;
        width: 100% !important;
    }
}

.selector {
    font-size: 30px;
    width: 650px;
    background-color: transparent;
    border-radius: 10px;
    border: solid 3px #FF8C00;
    padding: 10px;
    color: black;
    outline: none;
};



select::active {
    outline: none !important;
};

select::focus {
    outline: none !important;
};

</style>
