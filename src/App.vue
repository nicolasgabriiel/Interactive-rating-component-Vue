<template>
  <div class="background">
    <Card/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Card from "./components/Card.vue"

export default defineComponent({
  name: 'App',
  components: {
    Card,
  }
});
</script>
<style >
@import url(./reset.css);
@import url('https://fonts.googleapis.com/css2?family=Overpass&display=swap');

.background{
  font-family: 'Overpass';
  height: 100vh;

}



</style>

