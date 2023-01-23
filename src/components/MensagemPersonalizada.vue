<template>
    <p >{{msg}}</p>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
   name: "Mensagem-Personalizada",
   data(){
    return{
        msg: 'You selected 1 out of 5'
    }
   }
    
   
})
</script>
