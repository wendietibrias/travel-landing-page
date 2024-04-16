<script setup lang="ts">

 const { name,type,placeholder } = defineProps<{
    name:string;
    type:string;
    placeholder:string;
    items:string[];
 }>();

</script>

<template>

<div class="form-item">
  <select :type="type" :name="name" :placeholder="placeholder">
     <option v-for="(item,idx) in items" :key="idx">
       {{ item }}
    </option>
  </select>
</div>

</template>

<style scoped>

 .form-item {
  width:100%;
 }

 .form-item select {
   width:100%;
   border:solid 1px #AFB0B9;
   padding:0.8rem 1rem 0.8rem 0.8rem;
   border-radius:6px;
   color:#4A4C53;
   outline:none;
 }

</style>