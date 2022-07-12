<template>
<FormPedido/>
</template>

<script>
import FormPedido from './components/FormPedido.vue';

export default {
  name: 'App',
  components: { FormPedido },
};
</script>

<style>
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

} body{
  background-color: rgb(141, 14, 214);
  padding: 10px;
  margin: 0;
}
</style>
