<script setup>
import {counter} from "@/stores/CounterStore";
</script>

<template>
  <div>
    <p>
      About page. The current count is: {{ counter.count }}
    </p>
  </div>
</template>
