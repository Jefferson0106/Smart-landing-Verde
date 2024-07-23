<script setup>

import { onMounted, ref} from 'vue'

import axios from "axios";

const chooseus = ref([]);

onMounted(async () => {
  const { data: fetchedChooseus } = await axios.get("/data/choose-us.json");
  chooseus.value = fetchedChooseus.chooseus;
});


</script>

<template>
  
  
</template>

<style scoped>
  .contenedor {
      text-align: center;
      /* Personaliza otros estilos aquí */
  }
  .titulo{
    color: beige;
    font-size: 40px;
    top: 440px;
    left: -50px;
  }
  p{
    margin:  30px;
    color: beige;
    top: 440px;
    left: -20px;
  }
</style>