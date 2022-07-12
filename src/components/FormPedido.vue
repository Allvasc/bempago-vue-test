<template>
  <section class="body">
    <header>
      <div class="container-header">
        <h1>Formulário<br /> para compra de<br />
          <span>Pacotes adesivos</span>
        </h1>
        <img class="imgpkg" :src="require('../assets/package.svg')"
        alt="imagem de um pacote de entregas" />
      </div>
    </header>
    <form>
      <span class="txBold">Selecione os seus adesivos</span>
      <label for="react">
        <input type="checkbox" id="react" value="React" v-model="checkedNames">
        React
      </label>
      <label for="vue">
        <input type="checkbox" id="vue" value="Vue" v-model="checkedNames">
        Vue
      </label>
      <label for="angular">
        <input type="checkbox" id="angular" value="Angular" v-model="checkedNames">
        Angular
      </label>
      <br>
      <div class="container-buttom">
        <button class="buttonCount" type="button" v-on:click="decrement">-</button>
        <input class="InputCount" type="number" name="number" id="Number" v-model="number">
        <button class="buttonCount" type="button" v-on:click="increment">+</button>
      </div>
    </form>
  </section>
</template>

<script>
export default {
  data() {
    return {
      number: 0,
    };
  },
  methods: {
    increment() {
      this.number += 1;
    },
    decrement() {
      this.number -= 1;
    },
  },
};
</script>

<style>
.body {
  background: #fff !important;
  max-width: 450px;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: column;
  height: 96vh;
  margin: auto;
  border-radius: 10px;
  overflow: hidden;

}

header {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: left;
  overflow: hidden;
  margin-right: 30px;
  background-image: url('../assets/blob2.svg');
  background-size: 100%;
  background-position: center 88%;
  height: 200px;
  width: 1292px;

}

.container-header {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: left;
  width: 450px;
  margin: auto;
}

header h1 {
  margin: auto;
  color: #fff;
  align-self: flex-start;
  height: 150px;
  font-weight: 300;
}

header h1 span {
  margin: auto;
  color: #fff;
  align-self: flex-start;
  height: 150px;
  font-weight: 600;
  font-size: 1.6rem;
  line-height: 40px;
}

.imgpkg {
  width: 132px;
  margin: auto;
  opacity: 0.5;
  transform: rotate(-4deg) translate(5px, -10px);
}

form {
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  flex-direction: column;
  text-align: left;
  margin: 30px;
  width: 400px;
}

.txBold {
  font-weight: 600;
  font-size: 1.2rem;
  margin-bottom: 10px;
}

.container-buttom{
  display: flex;
  justify-content: center;
  align-items: center;
}

.buttonCount{
  background: rgb(255,137,2);
  background: linear-gradient(55deg, rgb(247, 177, 97) 0%, rgb(233, 165, 212) 81%);
  height: 35px;
  width: 35px;
  border-radius: 5px;
  border:none;
  font-size: 1.5rem;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
}

.InputCount{
  height: 25px;
  width: 35px;
  border-radius: 5px;
  font-size: 1.2rem;
  color: #000;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin: 0 10px;
}

</style>
