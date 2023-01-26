<template>
    <section>
    <h2>Thank you!</h2>
    <p>We appreciate you taking the time to give a rating. If you ever need more support, don't hesitate to get in touch!</p>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "Mensagem-de-gratificacao ",
    
})
</script>

<style scoped>
section{
    text-align: center;
}
h2{
    margin: 50px 0 20px 0;
    font-size: 25px;
    color: white;
    font-weight: bold;
}
p{
    font-size: 17px;
    color: #7F8591;
    margin: 0 30px;
    line-height: 20px;
}
</style>