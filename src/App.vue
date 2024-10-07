<script setup>
import NavBar from './components/Nav.vue';
import NavBar2 from './components/Nav-2.vue';
import MAIN from './components/Main.vue';
import Advantage from './components/Adv.vue';
import Platform from './components/Platform.vue';
import Ecosystem from './components/Eco.vue';
import Coins from './components/Coins.vue';
import Contact from './components/Contact.vue';
</script>

<template>
  <NavBar2/>
  <main>
    <MAIN/>
    <Advantage/>
    <Platform/>
    <Ecosystem/>
    <Coins/>
    <Contact/>
  </main>
</template>