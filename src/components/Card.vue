<template>
    <section>
        <h1><img src="../assets/icon-star.svg"/> </h1>
        <Texto/>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Texto from "./Texto.vue"

export default defineComponent({
    name: "card-component-interactive",
    components: ({
        Texto
    })

})
</script>

<style scoped> 
    section{
        height: 300px;
        background-image: radial-gradient(circle at 50% 0, #252C35 0%, #171E28 100%);
        border-radius: 40px;
    }
    h1{
        background-color: #262F38;
        display: inline-block;
        padding: 15px;
        margin: 40px;
        border-radius: 100px;
    }
    h1 img{
        width: 23px;
    }
</style>
