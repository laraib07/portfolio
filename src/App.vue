<script setup>
import { onBeforeMount, ref } from "vue";
import Header from "./partials/Header.vue";
import Hero from "./partials/Hero.vue";
import About from "./partials/About.vue";
import Experience from "./partials/Experience.vue";
import Portfolio from "./partials/Portfolio.vue";
import Skills from "./partials/Skills.vue";
import Contact from "./partials/Contact.vue";
import Footer from "./partials/Footer.vue";

const data = ref(null);

async function getData() {
  const res = await fetch("/portfolio/data/data.json").then((res) =>
    res.json()
  );
  data.value = res;
}

getData();
</script>

<template>
  <div v-if="data">
    <Header :resume-link="data['resume']" />
    <Hero />
    <About />
    <Experience :experience="data['experience']" />
    <Portfolio :projects="data['portfolio']" />
    <Skills :skills="data['skills']" />
    <Contact />
    <Footer />
  </div>
</template>
