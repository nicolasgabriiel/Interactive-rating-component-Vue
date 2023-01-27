<template>
    <section class="barra" >
        <li>
            <button @click="$emit('escolhido')" v-bind:class="{'ativado' : botaoHabilitado[0]}">1</button>
            <button @click="escolha(2)" v-bind:class="{'ativado' : botaoHabilitado[1]}">2</button>
            <button @click="escolha(3)" v-bind:class="{'ativado' : botaoHabilitado[2]}">3</button>
            <button @click="escolha(4)" v-bind:class="{'ativado' : botaoHabilitado[3]}">4</button>
            <button @click="escolha(5)" v-bind:class="{'ativado' : botaoHabilitado[4]}">5</button>
        </li>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'



export default defineComponent({
    name: "Barra-de-Escolha",
    data(){
        return{
            botaoHabilitado: [false,false,false,false,false],
            escolhido: 0    
        }
    },
    methods: {
        escolha(numero: number){
            
            

            for(let i = 0; i < this.botaoHabilitado.length; i++){
                this.botaoHabilitado[i] = false
            }
            this.botaoHabilitado[numero - 1] = true
            this.escolhido = numero
            return this.escolhido
            
        },
    }

   
})


</script>

<style scoped>
.barra{
    margin: 35px 40px;
    
}
.barra li{
    display: flex;
    justify-content: space-between;
}
.barra li button:hover{
    background-color: rgb(255,117,14);
    color: white;
    cursor: pointer
}
.barra li button{
    background-color: #262F38;
    color: #727983;
    border: none;
    font-size: 20px;
    font-weight: bold;
    width: 50px;
    height: 50px;
    border-radius: 30px;
    padding: 15px;
    transition: .5s;
}
.barra li .ativado{
    background-color: #7C8898;
    color: white;
}
</style>