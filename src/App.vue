<script setup>
import { reactive } from 'vue';
import Cabecalho from './components/Cabecalho.vue';
import Calculo from './components/Calculo.vue';

const operacao = reactive({
  filtro: '+',
  n1: 0,
  n2: 0,
})

const operacoes = () => {
  const filtro = operacao.filtro;

  switch (filtro) {
    case '-':
      return operacao.n1 - operacao.n2;
    case '*':
      return operacao.n1 * operacao.n2;
    case '/':
      return operacao.n1 / operacao.n2;
    default:
      return operacao.n1 + operacao.n2;   
  }
}
</script>

<template>
  <div class="container">
   <Cabecalho />
   <Calculo :operacao="operacao" :resultado="operacoes()" />
  </div>
</template>