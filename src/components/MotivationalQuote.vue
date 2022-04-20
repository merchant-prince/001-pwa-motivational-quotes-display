<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{ quote: string }>();
</script>

<template>
  <article
    class="bg-white w-1/2 p-8 shadow-lg rounded-lg font-cursive text-3xl text-gray-800 cursor-pointer"
  >
    {{ props.quote }}
  </article>
</template>
