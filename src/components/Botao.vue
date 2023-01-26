<template>
    <section class="botao">
        <button @click="mudartela">submit</button>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "Botao-de-Chamada",
    methods:{
    mudartela(){
      this.hide = true
    }
  },
  data(){
    return{
      hide: false
    }
  },
})
</script>

<style scoped>
.botao{
    margin: 0 40px;
}
.botao button{
    margin-bottom: 50px;
    width: 100%;
    border: none;
    padding: 15px 0;
    color: white;
    background-color:rgb(255,117,14);
    font-size: 16px;
    font-weight: bold;
    border-radius:100px;
    text-transform: uppercase;
    letter-spacing: 3px;
    transition: .5s;
}
.botao button:hover{
    background-color: white;
    color:rgb(255,117,14);
    cursor: pointer;
}
</style>
