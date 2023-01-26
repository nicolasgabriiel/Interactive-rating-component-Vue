<template>
    <div class="capsula"><p class="mensagemPersonalizada">You selected {{NumeroEscolhido}} out of 5</p></div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
   name: "Mensagem-Personalizada",
   data(){
    return{
        numero: 1,
    }
   },
   props:{
    NumeroEscolhido:{
    type:Number,
    required: true
    
    }
   }
    
   
})
</script>

<style scoped>
.capsula{
    text-align: center;
}
.mensagemPersonalizada{
    background-color: #262F38;
    display: inline-block;
    padding: 10px 20px;
    border-radius: 20px;
    color: #FF760D;
    font-size: 16px;

}
</style>
