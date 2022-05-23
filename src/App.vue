<template>
  <header>
    <CabecalhoNotificacao />
  </header>
  <main>
    <BarraLateral />
    <div class="conteudo">
      <BuscaCep @aoEncontrarCep="adicionaCep" />

      <div class="lista_cep">
        <Ceps v-for="(cep, index) in ceps" :key="index" :cep="cep.cep"/>
      </div>

      <BotaoGerarEnderecos @aoGerarEnderecos="adicionaCard"/>

      <div class="cards">
        <CardsCep v-for="(card, index) in cards" :key="index" :arrayCeps="cepsGerados" :posicao="index"/>
      </div>

    </div>
  </main>
</template>

<script>
import CabecalhoNotificacao from './components/Cabecalho.vue';
import BarraLateral from './components/BarraLateral.vue';
import BuscaCep from './components/BuscaCep.vue';
import Ceps from './components/Ceps.vue'
import CardsCep from './components/CardsCep.vue';
import BotaoGerarEnderecos from './components/BotaoGerarEnderecos.vue';

export default {
  name: 'App',
  components: {
    CabecalhoNotificacao,
    BarraLateral,
    BuscaCep,
    Ceps,
    CardsCep,
    BotaoGerarEnderecos
},
  data () {
    return {
      ceps: [],
      cepsGerados: [],
      cards: []
    }
  },
  methods: {
    adicionaCep (cep){
      this.ceps.push(cep);
      this.cepsGerados.push(cep)
      
      
    },
    adicionaCard (card){
      this.cards.push(card);
      
      console.log(this.cepsGerados[0].cep.logradouro);
    }
  }
}
</script>

<style scoped>
main {
  display: flex;
}

.conteudo {
  margin-left: 3rem;
  max-width: 50%;
}
</style>
