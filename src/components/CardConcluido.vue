<template>
    <section class="card">
        <img src="../assets/illustration-thank-you.svg">
        <div class="capsula">
            <p class="mensagemPersonalizada">You selected {{ valorEsperado }} out of 5</p>
        </div>
        <section>
            <h2>Thank you!</h2>
            <p>We appreciate you taking the time to give a rating. If you ever need more support, don't hesitate to get
                in touch!</p>
        </section>

    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "card-complete",
    props: {
        valorEsperado: {
            type: Number,
            default: 0,
        }
    }
})
</script>

<style scoped>
.card {
    background-image: radial-gradient(circle at 50% 0, #252C35 0%, #171E28 100%);
    border-radius: 40px;
    width: 430px;
    height: 473.64px;
}

.card h1 {
    background-color: #262F38;
    display: inline-block;
    padding: 15px;
    margin: 40px;
    border-radius: 100px;
}

.card img {
    display: flex;
    margin: 0 auto;
    padding: 50px 0 30px 0;
    width: 40%;
}

.capsula {
    text-align: center;
}

.mensagemPersonalizada {
    background-color: #262F38;
    display: inline-block;
    padding: 10px 20px;
    border-radius: 20px;
    color: #FF760D;
    font-size: 16px;

}

section {
    text-align: center;
}

h2 {
    margin: 50px 0 20px 0;
    font-size: 25px;
    color: white;
    font-weight: bold;
}

p {
    font-size: 17px;
    color: #7F8591;
    margin: 0 30px;
    line-height: 20px;
}
</style>