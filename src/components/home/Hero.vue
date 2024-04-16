<script setup lang="ts">

import illustrationHero from "../../assets/images/hero-illustration.png";
import FillButton from "../global/FillButton.vue";
import Select from "../global/Select.vue";

</script>

<template>

 <section class="hero--container">
     <div class="hero--container-content">
         <div class="content-left">
            <h1>Explore and Travel</h1>
            <div class="search-form--container">
               <h5>Holiday finder</h5>
               <form class="form">
                   <Select type="text" name="location" placeholder="Location" :items="['Indonesia','Malaysia','Laos','Philiphina']" />
                   <Select type="text" name="location" placeholder="Location" :items="['Indonesia','Malaysia','Laos','Philiphina']" />
                   <Select type="text" name="location" placeholder="Location" :items="['Indonesia','Malaysia','Laos','Philiphina']" />
                   <Select type="text" name="location" placeholder="Location" :items="['Indonesia','Malaysia','Laos','Philiphina']" />
               </form>
               <FillButton title="Explore"/>
            </div>
         </div>
         <div class="content-right">
            <img :src="illustrationHero" alt="illustration-hero">
         </div>
     </div>
 </section>

</template>

<style scoped>

 .hero--container {
    min-height:100vh;
    width:100%;
    display:flex;
    align-items:center;
 }

 .hero--container-content {
    max-width:1100px;
    width:100%;
    margin:0 auto;
    display:flex;
    align-items:center;
    justify-content:space-between;
    column-gap:3rem;
    margin-top:2rem;
 }

 .content-left {
    width:420px;
 }

 .search-form--container {
    margin-top:3rem;
 }

 .search-form--container h5 {
    font-size:1rem;
    position:relative;
    width:max-content;
 }

 .search-form--container h5::after {
    content:"";
    position:absolute;
    bottom:-13px;
    left:0;
    width:40%;
    height:2px;
    background-color: var(--title-clr);
 }

 .search-form--container .form {
   display:grid;
   grid-template-columns:repeat(2,1fr);
   gap:1rem;
   margin:3rem 0 2rem;
 }

 .content-left h1 {
    font-size:3.5rem;
 }

 .content-right img {
    height:550px;
 }

 @media screen and (max-width:900px) {
   .hero--container-content {
       max-width:100%;
       padding:0 1.5rem;
   }
    .content-right img {
       width:400px;
       height:400px;
    }
 }

 @media screen and (max-width:840px) {
    .hero--container-content {
       flex-direction:column;
       row-gap:3rem;
       padding:0 2rem;
    }

    .content-left {
       width:100%;
    }

    .content-right img {
        width:100%;
        height:500px;
    }

    .content-left h1 {
      font-size:2.8rem;
    }
 }

 @media screen and (max-width:560px) {
   .hero--container-content {
       margin:7rem 0 0;
   }

   .content-left {
      width:100%;
   }

   .content-left h1 {
      font-size:2rem;
   }

   .search-form--container {
      margin-top:2rem;
   }

   .content-right img {
      width:100%;
      height:350px;
   }
 }

</style>