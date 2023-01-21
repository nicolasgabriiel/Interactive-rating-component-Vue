<template>
    <section class="card">
        <h1><img src="../assets/icon-star.svg"/> </h1>
        <Texto/>
        <Barra/>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Texto from "./Texto.vue"
import Barra from "./Barra.vue"

export default defineComponent({
    name: "card-component-interactive",
    components: ({
        Texto,
        Barra
    })

})
</script>

<style scoped> 
    .card{
        background-image: radial-gradient(circle at 50% 0, #252C35 0%, #171E28 100%);
        border-radius: 40px;
    }
    .card h1{
        background-color: #262F38;
        display: inline-block;
        padding: 15px;
        margin: 40px;
        border-radius: 100px;
    }
    .card h1 img{
        width: 23px;
    }
</style>
