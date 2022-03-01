<template>
  <section class="cards-clients">
    <div class="container">
      <div class="row g-sm-5">
        <div
          class="col-md-6 col-xl-4 container-cards"
          v-for="dog in dogs"
          v-bind:key="dog.id"
        >
          <div class="container__card">
            <div class="container__card__circle">
              <img :src="dog.image.url" alt="" />
            </div>
            <div class="container__card__content">
              <p>
                <span> Nombre: </span>
                {{ dog.name }}
              </p>
              <p>
                <span> Temperamento: </span>
                {{ dog.temperament }}
              </p>
              <p>
                <span> Longevidad: </span>
                {{ dog.life_span }}
              </p>
              <p>
                <span> Ancho: </span>
                {{ dog.weight.metric }} metros
              </p>
              <p>
                <span> Alto: </span>
                {{ dog.height.metric }} metros
              </p>
              <p>
                <span> Origen: </span>
                {{ dog.origin }}
              </p>

              <a href="#">Conoce su caso</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
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

img {
  width: 400px;
  height: 300px;
  transform: scale(0.999);
}

.cards-clients {
  background: linear-gradient(45deg, $secondary, $primary);
  margin: 0 !important;
  padding: 2rem;
  width: 100vw;
}

.container {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  overflow: hidden;
}


.container-cards {
  // padding: 1.5rem;
  &:hover .container__card {
    transform: scale(1.1);
  }
}

.container__card {
  position: relative;

  max-width: 350px;
  height: 575px;
  background: $white;
  margin: auto;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 15px 25px $shadow;
  transition: 0.5s;

  &__circle {
    position: relative;
    clip-path: circle(250px at center 0);
    width: 100%;
    height: 100%;
  }

  &__content {
    position: absolute;
    bottom: 10px;
    text-align: center;
    padding: 1rem;
    padding-top: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    p {
      color: $primary;
      font-family: $font-family-subtitle;

      > span {
        color: $secondary;
        font-family: $font-family-subtitle;
      }
    }

    a {
      margin-top: 1.5rem;
    }
    @include button-link;
  }
}

@include responsive(medium-screen) {
  .cards-clients {
    padding: 4rem 1rem;
  }

  .container {
    padding: 0rem !important;
  }

  .container-cards {
    padding: 2rem 0rem;
  }
}

@include responsive(small-screen) {
  .container__card {
    min-width: 285px;
    height: 575px;
  }
}

@include responsive(extra-small) {
  img {
    width: 285px;
    height: 250px;
  }

  .container__card {
    width: 265px;
    height: 575px;
  }
}
</style>
