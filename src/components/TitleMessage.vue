<template>
  <div class="message">
    <div class="title">
        <div class="word"><h1>Balkanoche</h1></div>
        <div class="word"><h1>Prison</h1></div>
        <div class="word"><h1>Calculator</h1></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TitleMessage",
  props: {
    msg: String,
  },
};
</script>

<style scoped>

.title {
    display: flex;
    flex-direction: row;
    border-left: solid black 6px;
    border-right: solid black 6px;
}

.word {
    display: flex;
    flex-direction: row;
    justify-content: center;
    width: 200px;
    border-left: solid black 6px;
    border-right: solid black 6px;
}

h1 {
  margin: 0 40px;
  line-height: 90px;
  color: black;
}

.message {
    border-top: solid black 4px;
    margin: 10px;
}
</style>
