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
    <form action="/sendform">
      <div class="container-checkbox">
          <span class="txBold">Selecione os seus adesivos</span><br />
        <div class="case-checkbox">
        <label for="react">
          <input type="checkbox" id="react" name="react" value="React" checked>
          React
        </label>
        <label for="vue">
          <input type="checkbox" id="vue" name="vue" value="Vue">
          Vue
        </label>
        <label for="angular">
          <input type="checkbox" id="angular" name="angular" value="Angular">
          Angular
        </label>
        </div>
      </div>

      <div class="container-buttom">
        <span class="txBold">Quantos adesivos de cada?</span><br />

        <div class="case-buttom">
        <button id="btnMenos" class="buttonCount" type="button" v-on:click="decrement">-</button>
        <label for="number">
          <input class="InputCount" type="number" min="1" name="number"
          id="Number" v-model="number">
        </label>
        <button class="buttonCount" type="button" v-on:click="increment">+</button>
        </div>
      </div>

      <div class="container-radio">
        <span class="txBold">Escolha a forma de pagamento</span><br />
        <div class="case-radio">
          <label for="credito">
            <input type="radio" id="credito" name="payment" value="Credito" checked />
            Cartão de crédito</label>

          <label for="boleto">
            <input type="radio" id="boleto" name="payment" value="Boleto" />
            Boleto</label>

          <label for="pix">
            <input type="radio" id="pix" name="payment" value="Pix" />
            Pix</label>
        </div>
      </div>

      <div class="container-textArea">
        <span class="txBold txAreaAligneTitle">Observações</span>
        <label for="mensagem">
          <textarea name="mensagem" placeholder="Alguma dúvida ou recado?"></textarea>
        </label>
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
      number: 1,
    };
  },
  methods: {
    increment() {
      this.number += 1;
    },
    decrement() {
      this.number -= 1;
      if (this.number < 1) {
        this.number = 1;
      }
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
  overflow: none;
  background: linear-gradient(55deg, #EA8781 0%, #D9689B 81%);
  height: 150px !important;
  width: 100%;
  border-bottom-left-radius: 30%;
  border-bottom-right-radius: 50%;
  overflow: hidden;

}

.container-header {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: left;
  height: 100%;
  width: 100%;
  margin: auto;
}

header h1 {
  margin: 10px auto auto auto;
  color: #fff;
  align-self: center;
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
  width: 80px;
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
  margin: auto 30px;
  width: 400px;
}

.container-checkbox{
  display: flex;
  justify-content: center;
  align-items: flex-start;
  flex-direction: column;
  margin: 10px 0 20px 0;
  width: 100%;
}
.container-checkbox .txBold {
  margin-bottom: 0;
  line-height: 10px;
}

.case-checkbox{
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: row;
  width: 100%;
}

.container-checkbox label{
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: row;
  padding: 0 20px 0 0;
}

#react,
#vue,
#angular {
  margin-top: 5px;
  padding-left: 20px;
}

input[type=checkbox] {
  position: relative;
  cursor: pointer;
  margin: 10px 20px 10px 0;
}

input[type=checkbox]:before {
  content: "";
  display: block;
  position: relative;
  width: 20px;
  height: 20px;
  top: 0;
  left: 0;
  background-color: #e9e9e9;
}

input[type=checkbox]:checked:before {
  content: "";
  display: block;
  position: relative;
  width: 20px;
  height: 20px;
  top: 0;
  left: 0;
  background-color: #1E80EF;
}

input[type=checkbox]:checked:after {
  content: "";
  display: block;
  width: 5px;
  height: 10px;
  border: solid white;
  border-width: 0 2px 2px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
  position: absolute;
  top: 2px;
  left: 6px;
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
  margin-bottom: 20px;
  flex-direction: column;
}
.container-buttom .txBold {
  margin-bottom: 0;
  }

.case-buttom{
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: row;
  width: 100%;
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
.container-textArea label{
  width: 100%;
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

.container-radio {
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  flex-direction: column;
}

.container-radio .txBold {
  margin-top: 10px;
  margin-bottom: 0;
  line-height: 0px;
}

.case-radio {
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  margin-top: 0;
}

.case-radio label {
  margin-right: 20px;
}

@media only screen and (max-width: 500px) {
  .body {
    background: #fff !important;
    max-width: 100%;
    height: 100vh;
    overflow: hidden;
  }

  header {
    justify-content: center;
    align-items: center;
    text-align: center;
    overflow: hidden;
    margin: 0;
    background-image: none;
    background: linear-gradient(55deg, #EA8781 0%, #D9689B 81%);
    height: 140px;
    width: 100%;

  }

  .container-header {
    width: 103vw;
  }

  header h1 {
    margin: 0px auto 0 auto;
    align-self: center !important;
  }

  header h1 span {
    font-size: 1.2rem;
  }

  .imgpkg {
    width: 100px;
    margin: 0 auto;
    transform: rotate(0) translate(0, -0px)
  }

  form {
    width: 350px;
    margin: 10px 30px;
  }

  .container-textArea textarea {
    width: 340px;
    height: 80px;
    padding: 10px 0 10px 10px;
  }
}

@media only screen and (max-width: 400px) {
  .body {
    height: 100vh;
    overflow: hidden;
  }

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
