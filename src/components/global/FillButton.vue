<script setup lang="ts">

 const { title } = defineProps(['title']);

</script>

<template>

   <button class="fill-button">{{ title }}</button>

</template>

<style scoped>

 .fill-button {
    padding:0.7rem 1.8rem;
    border-radius:6px;
    background-color: var(--primary-clr);
    color:var(--white-clr);
    font-weight:600;
 }

</style>