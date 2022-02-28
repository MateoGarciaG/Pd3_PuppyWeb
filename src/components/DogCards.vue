<template>
  <div class="hello">
    <ul>
      <li v-for="dog in dogs" v-bind:key="dog.id">
        <img :src="dog.image.url" alt="" />
        <br />
        <p>{{ dog.name }}</p>
        <p>{{ dog.temperament }}</p>
        <p>{{ dog.life_span }}</p>
        <p>{{ dog.weight }}</p>
        <p>{{ dog.height }}</p>
        <p>{{ dog.origin }}</p>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data: function () {
    return {
      dogs: {},
    };
  },
  created() {
    this.loadDogsData();
  },
  methods: {
    async loadDogsData() {
      try {
        // https://docs.thedogapi.com/api-reference/breeds/breeds-list
        const url = "https://api.thedogapi.com/v1/breeds?";

        const res = await fetch(
          url +
            new URLSearchParams({
              limit: 9,
            })
        );
        const dogs = await res.json();

        console.log(dogs);

        this.dogs = dogs;
      } catch (err) {
        console.log(err);
      }
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/scss/_constants.scss";

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

img {
  width: 400px;
  height: 300px;
  transform: scale(0.999);
}
</style>
