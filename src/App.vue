<script setup>
import CustomFooter from "@/components/CustomFooter.vue";
import Navbar from "@/components/navbarComponements/Navbar.vue";
import MobileNavbar from "@/components/navbarComponements/MobileNavbar.vue";
import Background from "@/components/Background.vue";
import {timeTheme} from "@/assets/js/themeMgmt";
import {ref} from "vue";
import {prettyCode} from "@/assets/js/prettyCode";
import PrettyButton from "@/components/PrettyButton.vue";


let scroll = ref(0);
window.addEventListener("scroll", () => {
  scroll.value = window.scrollY;
});

timeTheme();

let prettyWitness = ref(false);

let pretty = new prettyCode(prettyWitness);
pretty.initialize();
</script>

<template>
  <PrettyButton v-if="prettyWitness" @update:buttonClicked="pretty.stopPretty()"/>
  <Navbar :has-scrolled="scroll > 8" alignRight="true"/>
  <MobileNavbar :has-scrolled="scroll > 8"/>
  <Background :is-full="$route.name === 'Home'"/>
  <div class="page">
    <router-view></router-view>
  </div>
  <CustomFooter/>
</template>

<style scoped>
@media screen and (orientation: landscape) {
  .page {
    margin: 20vh 0 16vh;
  }
}

@media screen and (orientation: portrait) {
  .page {
    margin: 16vh 0 12vh;
  }
}
</style>

