
<script setup lang="ts">

import chevronRight from "../../assets/icons/chevron-right.png";
import trendingStories from "../../common/constants/trending_stories";


</script>

<template>

<section class="trending-stories--container">
    <div class="trending-stories--container-header">
         <h2>Trending Stories</h2>
         <button>View all <img :src="chevronRight" alt="chevron right" /> </button>
    </div>
    <div class="trending-stories--items">
        <div v-for="(item,idx) in trendingStories" :key="idx" class="trending-stories--item">
            <img :src="item.image" :alt="item.title" />
            <div class="trending-stories--item-desc">
                <h4>{{ item.title }}</h4>
                <p>{{item.description}}</p>
                <button>Read More</button>
            </div>
        </div>
    </div>
</section>

</template>

<style scoped>

.trending-stories--container {
    max-width:1100px;
    margin:0 auto;
    padding:6rem 0;
}

.trending-stories--container-header {
    display:flex;
    align-items:center;
    justify-content:space-between;
}

.trending-stories--container-header button{
   color:var(--primary-clr);
   font-weight:600;
   display:flex;
   column-gap:0.5rem;
   align-items:center;
}

.trending-stories--items {
    display:grid;
    grid-template-columns:repeat(4,1fr);
    margin-top:3rem;
    gap:1.5rem;
}

.trending-stories--item img {
    height:245px;
    width:100%;
    object-fit:fill;
    border-radius:8px;
}

.trending-stories--item-desc {
    padding:1rem 0;
    padding-right:1rem;
}

.trending-stories--item-desc h3 {
    font-size:1.2rem;
}

.trending-stories--item-desc p {
    font-size:0.85rem;
    margin:0.5rem 0 1rem;
    color:var(--subtitle-alt-clr);
    line-height:1.2rem;
}

.trending-stories--item-desc button {
    color:var(--primary-clr);
    font-weight:600;
    font-size:0.85rem;
}

@media screen and (max-width:900px) {
   .trending-stories--container {
     max-width:100%;
     padding:6rem 1.5rem;
   }


   .trending-stories--items {
    grid-template-columns:repeat(2,1fr);
    gap:1.5rem;
   }
}

@media  screen and (max-width:560px) {
  .trending-stories--container {
    padding:4rem 1.5rem;
  }

  .trending-stories--items {
    grid-template-columns:repeat(1,1fr);
    gap:1.5rem;
 }

 .trending-stories--container-header h2{
     font-size:1.3rem;
 }

}
</style>