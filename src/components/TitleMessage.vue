<template>
  <div class="message">
    <h1>{{ msg }}</h1>
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
h1 {
  margin: 0 40px;
  line-height: 100px;
  color: black;
}
</style>
