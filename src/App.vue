<script>
export default {
  data() {
    return {
      valorConta: 0,
      gorjeta: 20,
      numPessoas: 1,
    };
  },
};
</script>
<template>
  <header id="header"><h1>Calculadora de Gorjeta</h1></header>
  <main id="main">
    <div class="div-forms">
      <div class="form-area">
        <section class="form">
          <p>Valor da conta</p>
          <input type="number" placeholder="Valor" v-model="valorConta" />
        </section>
        <section class="form">
          <p>Pagantes</p>
          <input type="number" placeholder="Quantidade" v-model="numPessoas" />
        </section>
        <section class="form">
          <p>Avaliação</p>
          <select class="feedback" v-model="gorjeta">
            <option value="5">Péssimo</option>
            <option value="10">Ruim</option>
            <option value="15">Ok</option>
            <option value="20">Bom</option>
            <option value="25">Ótimo</option>
            <option value="30">Excelente</option>
          </select>
        </section>
      </div>
      <div class="form-result">
        <h1>
          Valor por pessoa: R${{
            (this.valorConta + (this.gorjeta / 100) * this.valorConta) /
            this.numPessoas
          }}
        </h1>
        <p class="gorjeta">
          Gorjeta: R${{ (this.gorjeta * this.valorConta) / 100 }} ({{
            this.gorjeta
          }}%)
        </p>
      </div>
    </div>
  </main>
</template>
<style>
* {
  margin: 0px;
  padding: 0px;
}
#app {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 8vh 92vh;
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
  color: white;
}
#main {
  display: flex;
  justify-content: center;
  padding: 5vh;

  background: linear-gradient(
    0deg,
    rgba(0, 0, 0, 1) 0%,
    rgba(45, 45, 45, 1) 100%
  );
  color: white;
}
.div-forms {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10vh;
  padding: 5vh;
  height: fit-content;
  border: 2px ridge white;
  border-block: none;
}
.form-area {
  display: flex;
  flex-direction: row;
  gap: 10px;

  font-size: 1.5rem;
}
.form {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.form-result {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: rgb(97, 255, 97);
}
input,
select {
  text-align: center;
  padding: 5px;
}
.gorjeta {
  color: rgb(82, 192, 255);
}
</style>
