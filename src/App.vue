<script>
export default {
  data() {
    return {
      gorjeta: "",
    };
  },
  methods: {},
};
</script>
<template>
  <header id="header"><h1>Calculadora de Gorjeta</h1></header>
  <main id="main">Oi</main>
</template>
<style>
* {
  margin: 0px;
  padding: 0px;
}
#app {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 8vh 1fr;
}
#header {
  background: linear-gradient(
    0deg,
    rgba(255, 0, 0, 1) 0%,
    rgba(45, 10, 10, 1) 50%
  );
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
#main {
  background: linear-gradient(
    0deg,
    rgba(0, 0, 0, 1) 0%,
    rgba(45, 45, 45, 1) 100%
  );

  min-height: 92vh;
}
</style>
