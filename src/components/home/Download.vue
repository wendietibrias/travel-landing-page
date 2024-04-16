
<script setup lang="ts">

 import downloadIllustration from "../../assets/images/app-download-illustration.png";
import FillButton from "../global/FillButton.vue";

</script>

<template>

 <section class="download--container">
     <div class="download--container-left">
        <h2>Guides by Thousand Sunny</h2>
        <p>Packed with tips and advice from our on-the-ground experts, our city guides app (iOS and Android) is the ultimate resource before and during a trip.</p>
        <FillButton title="Download"/>
     </div>
     <div class="download--container-right">
        <img :src="downloadIllustration" alt="download illustration" />
     </div>
 </section>

</template>

<style scoped>

 .download--container {
    max-width:1100px;
    padding:6rem 0;
    margin:0 auto;
    display:flex;
    justify-content:space-between;
    align-items:center;
    column-gap:5rem;
 }

 .download--container-left {
    width:450px;
 }

 .download--container-left h2 {
    font-size:2rem;
 }

 .download--container-left p{
    color:var(--subtitle-clr);
    margin:1.5rem 0 2rem;
    line-height:1.5rem;
    font-size:1rem;
 }

 @media screen and (max-width:900px) {
     .download--container {
         max-width:100%;
         padding:6rem 1.5rem;
      }

      .download--container-right img {
         width:400px;
         height:400px;
      }
 }

 @media screen and (max-width:840px) {
    .download--container {
       column-gap:3rem;
    }

    .download--container-left h2 {
         font-size:1.5rem;
     }
 }

  @media screen and (max-width:560px) {
      .download--container {
         padding:4rem 1.5rem;
         flex-direction: column;
         row-gap:3rem;
      }

      .download--container-left {
         width:100%;
      }

      .download--container-right img {
         width:100%;
         height:350px;
      }

      .download--container-left h2 {
         font-size:1.3rem;
     }
  }
</style>