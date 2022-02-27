<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
  <div class="home">
    <DogCards />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import DogCards from "@/components/DogCards.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
    DogCards,
  },
};
</script>
