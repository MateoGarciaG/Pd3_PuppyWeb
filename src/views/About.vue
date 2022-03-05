<template>
  <Header />

  <Main
    title="Conoce más sobre nosotros"
    subtitle="Descubre lo que tu mascota quiere"
    imgBackground="about/about_banner.jpg"
  />

    <DogCards />

  <Footer />
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import DogCards from "@/components/DogCards.vue";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import Main from "@/components/Main.vue";


export default {
  name: "Home",
  components: {
    DogCards,
    Header,
    Footer,
    Main,
  },
};
</script>

<style scoped lang="scss">
@import "@/scss/_constants.scss";

</style>
