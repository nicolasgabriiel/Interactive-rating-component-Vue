<template>
    <section class="texto">
        <h2>How did we do?</h2>
        <p>Please let us know how we did with your support request. All feedback is appreciated to help us improve our offering!</p>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "Texto-card",
})
</script>

<style scoped>
.texto{
    padding: 0 40px;
}
.texto h2{
    color: white;
    font-size: 30px;
    margin-bottom: 15px;

}
.texto p{
    color: #727983;
    width: 350px;
    line-height: 25px;
}
</style>