
<script setup lang="ts">

import aboutIllustration from "../../assets/images/about-illustration.png";  
import FillButton from "../global/FillButton.vue";

</script>

<template>

 <section class="about--container">
     <div class="about--container-left">
        <img :src="aboutIllustration" alt="about" />
     </div>
     <div class="about--container-right">
        <h2>A new way to explore the world </h2>
        <p>For decades travellers have reached for Lonely Planet books when looking to plan and execute their perfect trip, but now, they can also let Lonely Planet Experiences lead the way</p>
        <FillButton title="Learn More"/>
     </div>
 </section>

</template>

<style scoped>

 .about--container {
     max-width:1100px;
     margin:0 auto;
     display:flex;
     align-items: center;
     padding:6rem 0;
     justify-content:space-between;
     column-gap:5rem;
 }


 .about--container-right {
    width:450px;
 }

 .about--container-right p {
    color:var(--subtitle-clr);
    line-height:1.5rem;
    font-size:1rem;
    margin:1.5rem 0 2rem;
 }

 .about--container-right h2 {
    font-size:2rem;
 }

 @media screen and (max-width:900px) {
    .about--container {
       max-width:100%; 
       padding:6rem 1.5rem;
    }

    .about--container-left img {
       width:400px;
       height:400px;
    }
 }

 @media screen and (max-width:840px) {
    .about--container-right h2 {
       font-size:1.5rem;
    }

    .about--container {
       column-gap:3rem;
    }
 }

 @media screen and (max-width:560px) {
   .about--container {
      flex-direction:column;
      row-gap:3rem;
   }

   .about--container-right h2 {
    font-size:1.3rem;
   } 

   .about--container-right {
      width:100%;
   }

   .about--container-left img {
       width:100%;
       height:350px;
   }
 }

</style>