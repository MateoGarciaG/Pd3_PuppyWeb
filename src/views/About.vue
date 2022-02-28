<template>
  <Header />
  <div class="home">
    
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
import Header from "@/components/Header.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
    DogCards,
    Header,
  },
};
</script>
