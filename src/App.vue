<template>
  <header>
    <CabecalhoNotificacao />
  </header>
  <main>
    <BarraLateral />
    <div class="conteudo">
      <BuscaCep />
      <ListaCeps />
      <CardsCep />
    </div>
  </main>
</template>

<script>
import CabecalhoNotificacao from './components/Cabecalho.vue';
import BarraLateral from './components/BarraLateral.vue';
import BuscaCep from './components/BuscaCep.vue';
import ListaCeps from './components/ListaCeps.vue';
import CardsCep from './components/CardsCep.vue';


export default {
  name: 'App',
  components: {
    CabecalhoNotificacao,
    BarraLateral,
    BuscaCep,
    ListaCeps,
    CardsCep
}
}
</script>

<style scoped>
main{
  display: flex;
}

.conteudo{
  margin-left: 3rem;
  max-width: 50%;
}

</style>
