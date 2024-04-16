<script setup lang="ts">

 import testimonialPeople from "../../assets/images/testimonial-people.png";
 import starRating from "../../assets/icons/star-rating.png";
 import arrowLeft from "../../assets/icons/arrow-left.svg";
 import arrowRight from "../../assets/icons/arrow-right.svg";

</script>

<template>

 <section class="testimonial--container">
     <h2>Testimonials</h2>
     <div class="testimonial--container-content">
        <div class="content-left">
           <img :src="starRating" alt="stars rating"/>
           <p>“Quisque in lacus a urna fermentum euismod. Integer mi nibh, dapibus ac scelerisque eu, facilisis quis purus. Morbi blandit sit amet turpis nec”</p>

           <div class="content-left-testi-user-info">
              <h5>Edward Newgate</h5>
              <h6>Founder Circle</h6>
           </div>
        </div>
        <div class="content-right">
            <img :src="testimonialPeople" alt="testimonial-people"/>
            <div class="next-prev-buttons-container">
                 <button class="disabled"><img :src="arrowLeft" alt="prev" style="width:24px; height:24px;" /></button>
                 <button><img :src="arrowRight" alt="right" style="width:24px; height:24px;"/></button>

            </div>
        </div>
     </div>
 </section>

</template>

<style scoped>

 .testimonial--container {
     max-width:1000px;
     margin:0 auto;
     padding:6rem 0;
 }

 .testimonial--container h2 {
    font-size:2rem;

 }

 .testimonial--container-content {
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-top:3rem;
 }

 .content-left {
    width:450px;
 }

 .content-left p {
    font-size:1.2rem;
    font-weight:400;
    margin:2rem 0 0;
 }

 .content-left-testi-user-info {
    margin:2rem 0 0;
 }

 .content-left-testi-user-info h5 {
    font-size:1.1rem;
 }

 .content-left-testi-user-info h6 {
    font-size:0.85rem;
    margin:0.4rem 0 0;
    font-weight:400;
 }

 .content-right {
    position:relative;
 }

.next-prev-buttons-container {
    width:max-content;
    background-color:#fff;
    position:absolute;
    bottom:0;
    display:flex;
    align-items: center;
    column-gap:1rem;
    right:0;
    padding:0.7rem;
}

.next-prev-buttons-container button {
    width:32px;
    height:32px;
    border:solid 2px var(--title-clr);
    border-radius:100px;
}

@media screen and (max-width:900px) {
   .testimonial--container {
     max-width:100%;
     padding:6rem 1.5rem;
  }

  .testimonial--container-content {
   column-gap:3rem;
  }
}

@media screen and (max-width:560px) {
   .testimonial--container {
     padding:4rem 1.5rem;
  }

  .testimonial--container-content {
    flex-direction:column;
    margin-top:3rem;
    row-gap:3rem;
  }

 .content-left {
    width:100%;
  }

  .content-right img {
   width:100%;
  }

  .testimonial--container h2 {
    font-size:1.3rem;
  }

}

</style>