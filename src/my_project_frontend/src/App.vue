<script setup>
import { ref } from 'vue';
import { my_project_backend } from 'declarations/my_project_backend/index';


const getDataFromNBP = async () => {
  const res = await fetch("https://api.nbp.pl/api/exchangerates/tables/A/?format=json")
  const jasonData = await res.json();
  console.log(jasonData)
  const rates = jasonData[0].rates
  console.log(rates)
}
getDataFromNBP()
</script>

<template>
  <main>
      
  </main>
</template>
