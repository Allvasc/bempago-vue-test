<template>
  <FormPedido />
</template>

<script>
import FormPedido from './components/FormPedido.vue';

export default {
  name: 'App',
  components: { FormPedido },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin: 0;
  padding: 0;

}

body {
  background-color: #8d0ed6;
  padding: 0;
  margin: 10px 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

@media only screen and (max-width: 500px) {
  body {
    background-color: #fff;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
}
</style>
