<template>
    <section class="barra">
        <li>
            <ul><button>1</button></ul>
            <ul><button>2</button></ul>
            <ul><button>3</button></ul>
            <ul><button>4</button></ul>
            <ul><button>5</button></ul>
        </li>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "Barra-de-Escolha",
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
.barra li ul{
    width: 22px;
    height: 22px;
    border-radius: 30px;
    background-color: #262F38;
    padding: 15px;
    transition: .5s;
}
.barra li ul:hover{
    background-color: rgb(255,117,14);
    cursor: pointer;
}
.barra li ul:hover button{
    color: white;
    cursor: pointer
}
.barra li ul button{
    background: transparent;
    color: #727983;
    border: none;
    font-size: 20px;
    font-weight: bold;
}
</style>