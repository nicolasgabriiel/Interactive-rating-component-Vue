<template>
    <section class="card">
        <h1><img src="../assets/illustration-thank-you.svg"> </h1>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "card-complete",

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