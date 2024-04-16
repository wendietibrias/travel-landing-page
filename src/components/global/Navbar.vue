
<script setup lang="ts">

import navbarLinks from "../../common/constants/navbar_links";
import companyLogo from "../../assets/images/company-logo.png";
import FillButton from "./FillButton.vue";
import OutlineButton from "./OutlineButton.vue";
import { ref } from "vue";

const isShowSidebar = ref<boolean>(false);

const handleShowSidebar = () => isShowSidebar.value = !isShowSidebar.value;

</script>

<template>
    <nav class="navbar--container">
        <div class="navbar--container-content">
            <img v-bind:src="companyLogo" alt="company logo">
            <div class="navbar--container-content-right" :class="{active: isShowSidebar}">
                <ul class="navbar-links">
                    <li v-for="(item,index) in navbarLinks" :key="item.title">
                        <a :href="item.path" :class="{ active: index===0 ? true : false }">{{ item.title }}</a>
                    </li>
                </ul>
                <div class="navbar-buttons">
                     <OutlineButton title="Login"/>
                     <FillButton title="Register" />
                </div>
            </div>
             <button v-on:click="handleShowSidebar" id="menu-hamburger">
               <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="18" height="18" fill="currentColor"><path d="M3 4H21V6H3V4ZM9 11H21V13H9V11ZM3 18H21V20H3V18Z"></path></svg>            
             </button>
        </div>
    </nav>
</template>

<style scoped>

  .navbar--container {
    width:100%;
    background-color: var(--white-clr);
    padding:1.5rem 0;
    position:fixed;
    top:0;
    z-index:9999;
    left:0;
  }

  .navbar--container-content {
     max-width:1100px;
     display:flex;
     justify-content:space-between;
     align-items:center;
     margin:0 auto;
  }

  .navbar--container-content-right{
    display:flex;
    align-items:center;
    column-gap:2.5rem;
  }

  .navbar-links{
    display:flex;
    align-items:center;
    list-style:none;
    column-gap:1.8rem;
  }

  .navbar-links li a {
    font-size:0.9rem;
    color:#B8BECD;
  }

  .navbar-links li a.active {
    color:var(--black-clr);
    font-weight:600;
  }

  .navbar-buttons{
    display:flex;
    column-gap:1rem;
  }

  #menu-hamburger {
    display:none;
  }

  @media screen and (max-width:900px) {
     .navbar--container-content {
         padding:0 1.5rem;
     }
  }

  @media screen and (max-width:560px) {

    .navbar--container-content {
       max-width:100%;
    }

    .navbar--container-content-right {
        position:fixed;
        top:0;
        left:-100%;
        transition: all 0.4s ease-in-out;
        height:100vh;
        width:80%;
        flex-direction:column;
        justify-content: flex-start;
        align-items: flex-start;
        background:var(--white-clr);
        z-index:99999;
        padding:1.5rem;
        row-gap:1.5rem;
    }

    .navbar--container-content-right.active {
      left:0;
    }

    .navbar-links {
      align-items: flex-start;
      row-gap:0.8rem;
      flex-direction: column;
    }

     #menu-hamburger {
      display:block;
    }

    
  }
</style>