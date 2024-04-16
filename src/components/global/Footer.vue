<script setup lang="ts">

import companyLogo from "../../assets/images/company-logo.png";
import footerLinks from "../../common/constants/footer_links";

</script>

<template>
    <footer class="footer--container">
        <div class="footer--container-content">
             <div class="company-description">
                 <img :src="companyLogo" alt="company logo"/>
                 <p>Plan and book your perfect trip with expert advice, travel tips destination information from us</p>
                 <h5>©2020 Thousand Sunny. All rights reserved</h5>
             </div>
             <div class="footer-link"  v-for="(item,idx) in footerLinks" :key="idx">
                  <h5>{{ item.title }}</h5>
                  <ul>
                     <li v-for="(link,idxLink) in item.items" :key="idxLink">
                         <span>{{ link }}</span>
                     </li>
                  </ul>
             </div>
        </div>
    </footer>
</template>

<style scoped>

 .footer--container {
    background-color:#F9F9FB;
    padding:3rem 0;
 }

 .footer--container-content {
    max-width:1100px;
    margin:0 auto;
    display:flex;
    justify-content:space-between;
    flex-wrap:wrap;
    align-items:flex-start;
 }

 .company-description {
    width:300px;
 }

 .company-description p {
    font-size:1rem;
    color:var(--subtitle-alt-clr);
    margin:1rem 0 2rem;
    font-weight:400;
 }

 
 .company-description h5 {
    font-weight:400;
    color:var(--subtitle-alt-clr);
    font-size:0.8rem;
 }

 .footer-link h5 {
    font-size:1rem;
    font-weight:600;
 }

.footer-link ul {
    list-style:none;
    display:flex;
    flex-direction: column;
    row-gap:0.7rem;
    margin-top:1.5rem;
}

.footer-link ul span {
    color:var(--subtitle-alt-clr);
    font-weight:400;
    font-size:0.9rem;
}

@media screen and (max-width:900px) {
   .footer--container-content {
      max-width:100%;
      padding:0 1.5rem;
   }
}

@media screen and (max-width:840px) {
   .footer--container-content {
      row-gap:2rem;
   }

   .footer-link {
      width:40%;
   }

   .company-description {
      width:40%;
   }
}

@media screen and (max-width:560px) {
   .footer--container-content {
      flex-direction: column;
      row-gap:2rem;
   }

   .footer-link,.company-description {
      width:100%;
   }
}
</style>