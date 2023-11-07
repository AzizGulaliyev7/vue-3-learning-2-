<script setup>
  import { state } from "@/stores/quizStore";
</script>

<template>
  <div>
    <h5>
       {{ state.name }}
    </h5>
    <button @click="state.name = 'new name'">Change quize name</button>

    <ul>
      <li><a href="#">Get a Job</a></li>
      <li><a href="#">Contact us</a></li>
    </ul>
  </div>
</template>

<style scoped>

</style>