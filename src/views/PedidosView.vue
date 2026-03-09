<template>
  <div class="main-container">
    <h1>Gerenciar Pedidos:</h1>
    <DashBoard />
  </div>
</template>

<script>

import DashBoard from '../components/DashBoard.vue';

export default {
  name: 'PedidosView',
  components: {
    DashBoard
  },
  data() {
    return {
      // Dados relacionados aos pedidos podem ser adicionados aqui
    };
  },
  methods: {
    // Métodos para gerenciar pedidos podem ser adicionados aqui
  }
};


</script>