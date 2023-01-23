<template>
    <p class="mensagemPersonalizada">You selected {{numero}} out of 5</p>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
   name: "Mensagem-Personalizada",
   data(){
    return{
        numero: 1,
    }
   }
    
   
})
</script>

<style scoped>
.mensagemPersonalizada{
    background-color: #262F38;
    display: inline-block;
    padding: 10px 20px;
    border-radius: 20px;
    color: #FF760D;
    font-size: 16px;
}
</style>
