<template>
  <div class="background" >
    <section v-bind:class ="{'hide': hide}">
      <Card v-on:hide="Funcao" v-on:valor="descobrirValor"/>
    </section>
    <section v-bind:class ="{'hide': !hide}">
      <CardConcluido :valor-esperado='valor' />
    </section>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Card from "./components/Card.vue"
import CardConcluido from "./components/CardConcluido.vue"


export default defineComponent({
  name: 'App',
  
  components: {
    Card,
    CardConcluido
  },
  data(){
    return{
      hide: false,
      valor: 0
    }
  },
  methods:{
    Funcao(){
      this.hide = true
    },
    descobrirValor(evento: any){
      this.valor = evento.meuValor
    }
  }
});
</script>





















<style >
@import url(./reset.css);
@import url('https://fonts.googleapis.com/css2?family=Overpass&display=swap');

.background{
  font-family: 'Overpass';
  height: 100vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #141519;
}
.hide {
  display: none !important; 
}



</style>

