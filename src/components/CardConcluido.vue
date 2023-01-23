<template>
    <section class="card">
        <img src="../assets/illustration-thank-you.svg"> 
        <MensagemPersonalizada/>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import MensagemPersonalizada from './MensagemPersonalizada.vue';

export default defineComponent({
    name: "card-complete",
    components: {
        MensagemPersonalizada
    }
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
        width: 50px;
    }
</style>