<template>
    <section>
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
section{
    padding: 0 40px;
}
h2{
    color: white;
    font-size: 30px;
    margin-bottom: 15px;

}
p{
    color: #727983;
    width: 350px;
    line-height: 25px;
}
</style>