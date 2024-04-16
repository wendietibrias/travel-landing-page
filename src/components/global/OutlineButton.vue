
<script setup lang="ts">
 
 const { title } = defineProps(['title']);

</script>

<template>

  <button class="outline-button">{{ title }}</button>

</template>

<style scoped>

.outline-button {
    padding:0.6rem 1.8rem;
    border-radius:6px;
    border: solid 2px var(--primary-clr);
    color:var(--primary-clr);
    font-weight:500;
 }


</style>