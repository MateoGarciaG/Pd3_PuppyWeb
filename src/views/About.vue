<template>
  <Header />

  <main>
    <div class="container">
      <div class="row">
        <div class="col">Column</div>
        <div class="col">Column</div>
        <div class="col">Column</div>
      </div>
    </div>
  </main>

  <div class="home">
    <DogCards />
  </div>

  <Footer />
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import DogCards from "@/components/DogCards.vue";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    DogCards,
    Header,
    Footer,
  },
};
</script>

<style scoped lang="scss">
@import "@/scss/_constants.scss";

main {
  height: 50vh;
}
</style>
