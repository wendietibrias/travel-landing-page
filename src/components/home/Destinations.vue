
<script setup lang="ts">

 import destinations from '../../common/constants/destinations';
 import chevronRight from "../../assets/icons/chevron-right.png";

</script>

<template>

<section class="destination--container">
    <div class="destination--container-header">
         <h2>Featured destinations</h2>
         <button>View all <img :src="chevronRight" alt="chevron right" /> </button>
    </div>
    <div class="destination--items">
        <div class="destination--item" v-for="(item,idx) in destinations" :key="idx">
            <img :src="item.image" :alt="item.name" />
            <div class="destination--item-desc">
                <h5>{{ item.name }}</h5>
                <h6>{{ item.country }}</h6>
            </div>
        </div>
    </div>
</section>

</template>

<style scoped>

 .destination--container {
     max-width:1100px;
     margin:0 auto;
     padding:6rem 0;
 }

.destination--container-header {
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.destination--container-header h2 {
    font-size:2rem;
}

.destination--container-header button {
    color:var(--primary-clr);
    font-weight:600;
    font-size:0.9rem;
}

.destination--container-header button img{
    margin-left:0.3rem;
}

.destination--items {
     display:grid;
     grid-template-columns:repeat(4,1fr);
     gap:1rem;
     margin-top:3rem;
}

.destination--item {
    position:relative;
}

.destination--item img {
    width:100%;
    object-fit:fill;
    border-radius:8px;
}

.destination--item-desc {
    position:absolute;
    bottom:0;
    left:0;
    width:max-content;
    border-top-right-radius: 8px;
    background-color:var(--white-clr);
    padding:0.7rem;

}

.destination--item-desc h6 {
    font-weight:500;
    color:var(--subtitle-alt-clr);
    margin-top:0.2rem;

}

@media screen and (max-width:900px) {
    .destination--container {
     max-width:100%;
     padding:6rem 1.5rem;
   }

}

@media screen and (max-width:560px) {


    .destination--container {
     max-width:100%;
     margin:0 auto;
     padding:4rem 1.5rem;
   }

    .destination--items {
        grid-template-columns: repeat(1,1fr);
    }

    .destination--container-header h2 {
       font-size:1.3rem;
   }
}

</style>