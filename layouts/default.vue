<template>
  <div>
    <Header />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css";

export default {
  mounted() {
    AOS.init({});
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@500&family=Playfair+Display:wght@400;700&display=swap");
</style>
