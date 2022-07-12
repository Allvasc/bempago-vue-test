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
        <input type="checkbox" id="react" value="React">
        React
      </label>
      <label for="vue">
        <input type="checkbox" id="vue" value="Vue">
        Vue
      </label>
      <label for="angular">
        <input type="checkbox" id="angular" value="Angular">
        Angular
      </label>
      <br>
      <div class="container-buttom">
        <button class="buttonCount" type="button" v-on:click="decrement">-</button>
        <input class="InputCount" type="number" name="number" id="Number" v-model="number">
        <button class="buttonCount" type="button" v-on:click="increment">+</button>
      </div>
      <div class="container-textArea">
        <span class="txBold txAreaAligneTitle">Observações</span>
        <textarea placeholder="Alguma dúvida ou recado?"></textarea>
      </div>
      <div class="container-submit">
        <input type="submit" value="Enviar">
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
  transform: rotate(-4deg) translate(5px, -15px);
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

.container-buttom {
  display: flex;
  justify-content: center;
  align-items: center;
}

.buttonCount {
  background: linear-gradient(55deg, #EA8781 0%, #D9689B 81%);
  height: 35px;
  width: 35px;
  border-radius: 5px;
  border: none;
  font-size: 1.5rem;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

.InputCount {
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
  border: 1px solid rgb(102, 102, 102);
}

/* Chrome, Safari, Edge, Opera */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
input[type=number] {
  -moz-appearance: textfield;
}

.container-textArea {
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  flex-direction: column;
  margin: 20px 0;
  width: 390px !important;
}

.txAreaAligneTitle {
  text-align: left;
}

.container-textArea textarea {
  width: 100%;
  height: 80px;
  border-radius: 5px;
  background-color: rgb(253, 238, 233);
  padding: 10px 0 10px 10px;
  align-self: left;
}

.container-submit {
  display: flex;
  justify-content: flex-end;
  align-items: flex-end;
  width: 100%;
}

.container-submit input {
  font-size: 1.2rem;
  background: linear-gradient(55deg, #EA8781 0%, #D9689B 81%);
  border: none;
  border-radius: 5px;
  height: 30px;
  width: 120px;
  cursor: pointer;
  color: #fff;
  transition: 0.5s ease-in-out;
}

.container-submit input:hover {
  background: #eb4e94;
  background: linear-gradient(55deg, #eb4e94 0%, #eb4e94 81%);
  }

@media only screen and (max-width: 500px) {
  .body {
    background: #fff !important;
    max-width: 100%;
  }

  header {
    justify-content: center;
    align-items: center;
    text-align: center;
    overflow: visible;
    margin: 0;
    background-image: none;
    background: linear-gradient(55deg, #EA8781 0%, #D9689B 81%);
    height: 130px;
    width: 100%;

  }

  .container-header {
    width: 100%;
  }

  header h1 {
    margin: 20px auto 0 auto;
    align-self: center !important;
  }

  header h1 span {
    font-size: 1.2rem;
  }

  .imgpkg {
    width: 100px;
    margin: 0 auto;
    transform: rotate(0) translate(0, -20px);
  }

  form {
    width: 350px;
  }

  .container-textArea textarea {
    width: 340px;
    height: 80px;
    padding: 10px 0 10px 10px;
  }
}

@media only screen and (max-width: 400px) {
  .container-textArea textarea {
    width: 320px;
    height: 80px;
    padding: 10px 0 10px 10px;
  }
  form {
    width: 330px;
}
}
</style>
