<script setup lang="ts">
 
 const { src,alt } = defineProps<{ src:string }>()

</script>

<template>
    <img :src="src" alt="image"/>
</template>