<script setup>
  import { state } from "@/stores/quizStore";
</script>

<template>
  <header>
    <h2>
      Quiz header
      {{ state.name }}
    </h2>
  </header>
</template>

<style scoped>

</style>