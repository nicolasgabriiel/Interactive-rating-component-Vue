<template>
  <div class="background" @click="mudartela">
    <section v-bind:class ="{'hide': hide}">
      <Card />
    </section>
    <section v-bind:class ="{'hide': !hide}">
      <CardConcluido/>
    </section>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Card from "./components/Card.vue"
import CardConcluido from "./components/CardConcluido.vue"

export default defineComponent({
  name: 'App',
  data(){
    return{
      hide: false
    }
  },
  methods:{
    mudartela(){
      this.hide = true
    }
  },
  components: {
    Card,
    CardConcluido
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

