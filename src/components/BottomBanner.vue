<template>
  <div class="banner">
    <span class="left">
        <p>Les données ont été calculées grâce aux informations trouvées sur <a href="https://fr.wikipedia.org/wiki/Affaire_Balkany" target="Affaire Balkany">Wikipedia</a> - Ratio de temps de prison de 2.19 secondes par euros volé</p>
        <p>Ce calculateur ne constitue absolument pas une réalité juridique. Fiez vous à <a href="https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006070719/"  target="Code pénal">Legifrance</a> pour ça</p>
    </span>
    <span class="right">
        <a href="https://twitter.com/YavaDeus" target="twiter">A propos de moi</a>
    </span>
  </div>
</template>

<script>

export default {
  name: "BottomBanner",
};
</script>

<style scoped>
.banner {
    position: absolute;
    bottom: 0px;
    width: 100%;
    height: 100px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    background-color : #FF8C00;
    border-top: solid black 4px;
}

@media (max-width: 1250px) {
    .banner {
        font-size: 10px;
        flex-direction: column;
        height: 50px;
    }
}

@media (max-width: 1250px) {
    .banner {
        position: relative;
    }
}

.left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-left: 20px;
}

.left > p {
    margin: 0;
    align-self: flex-start;
}

.right {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-right: 20px;
}

</style>
