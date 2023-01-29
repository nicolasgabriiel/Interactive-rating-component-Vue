<template>
    <section class="card">
        <h1><img src="../assets/icon-star.svg" /> </h1>
        <section class="texto">
            <h2>How did we do?</h2>
            <p>Please let us know how we did with your support request. All feedback is appreciated to help us improve
                our offering!</p>
        </section>
        <section class="barra">
            <li>
                <button @click="escolha(1)" v-bind:class="{'ativado' : botaoHabilitado[0]}">1</button>
                <button @click="escolha(2)" v-bind:class="{ 'ativado': botaoHabilitado[1] }">2</button>
                <button @click="escolha(3)" v-bind:class="{ 'ativado': botaoHabilitado[2] }">3</button>
                <button @click="escolha(4)" v-bind:class="{ 'ativado': botaoHabilitado[3] }">4</button>
                <button @click="escolha(5)" v-bind:class="{ 'ativado': botaoHabilitado[4] }">5</button>
            </li>
        </section>
        <section class="botao">
            <button @click="mudartela">submit</button>
        </section>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "card-component-interactive",
    components: ({
    }),
    data() {
        return {
            botaoHabilitado: [false, false, false, false, false],
            escolhido: 0,
        }
    },
    methods: {
        escolha(numero: number) {
            for (let i = 0; i < this.botaoHabilitado.length; i++) {
                this.botaoHabilitado[i] = false
            }
            this.botaoHabilitado[numero - 1] = true
            this.escolhido = numero
            this.$emit('valor', { meuValor: this.escolhido } )
        },
        mudartela() {
            if(this.escolhido === 0){
                alert('Choose a value from 1 to 5!')
            }else{
                this.$emit('hide')
            }
        }
    }



})
</script>

<style scoped>
.card {
    background-image: radial-gradient(circle at 50% 0, #252C35 0%, #171E28 100%);
    border-radius: 40px;
}

.card h1 {
    background-color: #262F38;
    display: inline-block;
    padding: 15px;
    margin: 40px;
    border-radius: 100px;
}

.card h1 img {
    width: 23px;
}

span {
    background: red;
    display: block !important;
}

.texto {
    padding: 0 40px;
}

.texto h2 {
    color: white;
    font-size: 30px;
    margin-bottom: 15px;

}

.texto p {
    color: #727983;
    width: 350px;
    line-height: 25px;
}

.barra {
    margin: 35px 40px;

}

.barra li {
    display: flex;
    justify-content: space-between;
}

.barra li button:hover {
    background-color: rgb(255, 117, 14);
    color: white;
    cursor: pointer
}

.barra li button {
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

.barra li .ativado {
    background-color: #7C8898;
    color: white;
}
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
