<template>
  <Header />

  <Main
    title="Bienvenidos al mundo puppy"
    subtitle="Conocenos!"
    imgBackground="home/home_banner.jpg"
  />

  <section class="section-parallax">
    <div class="parallax__content">
      <h3 class="display-4">Juntos mejoramos con los nuestros</h3>
      <Carousel :wrap-around="true">
        <Slide v-for="(slideSrc, i) in slideImages" :key="i">
          <div class="carousel__item">
            <img
              :src="require(`@/assets/img/home/${slideSrc}`)"
              :alt="'slide' + i"
            />
          </div>
        </Slide>
        <template #addons>
          <Navigation />
          <Pagination />
        </template>
      </Carousel>

      <p>
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Magnam
        architecto recusandae ipsa culpa quibusdam id. Ut qui sequi consequatur
        vero quo ex, repellat, amet exercitationem repellendus explicabo, nisi
        quae iure. Lorem ipsum dolor sit, amet consectetur adipisicing elit. In
        itaque sed expedita explicabo. Natus quidem delectus illo
      </p>
    </div>

    <!-- ***** next parallax ***** -->

    <div class="background-parallax" id="parallax-img-1">
      <div class="container-fluid background-parallax__content">
        <div class="row justify-content-xs-center justify-content-lg-around">
          <div
            class="col-lg-4 d-flex flex-column justify-content-center align-items-center"
          >
            <h3 class="display-4">Te ayudamos en lo que necesites</h3>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Necessitatibus, sequi maiores similique error, commodi cum
              accusamus voluptates corrupti quam blanditiis illum asperiores
              eligendi consequuntur tenetur eius pariatur illo. Nulla, a?
            </p>
          </div>
          <div class="col-lg-5 p-5">
            <img
              class="background-parallax__content__img"
              src="../assets/img/home/dog_vector1.svg"
              alt="vector_dog1"
            />
          </div>
        </div>
      </div>
    </div>

    <!-- ***** next parallax ***** -->

    <div class="parallax__content">
      <h3 class="display-3 mb-5">Nuestros Servicios</h3>
      <div class="container">
        <div class="row gy-5 d-flex align-items-center justify-content-center">
          <div class="col-lg-3 m-4">
            <div class="card">
              <div class="card-body d-flex flex-column">
                <h5 class="card-title p-2">Special title treatment</h5>
                <p class="card-text px-2 py-3">
                  With supporting text below as a natural lead-in to additional
                  content.
                </p>
                <a href="#" class="mx-2 align-self-center">Go somewhere</a>
              </div>
            </div>
          </div>
          <div class="col-lg-3 m-4">
            <div class="card">
              <div class="card-body d-flex flex-column">
                <h5 class="card-title p-2">Special title treatment</h5>
                <p class="card-text px-2 py-3">
                  With supporting text below as a natural lead-in to additional
                  content.
                </p>
                <a href="#" class="mx-2 align-self-center">Go somewhere</a>
              </div>
            </div>
          </div>
          <div class="col-lg-3 m-4">
            <div class="card">
              <div class="card-body d-flex flex-column">
                <h5 class="card-title p-2">Special title treatment</h5>
                <p class="card-text px-2 py-3">
                  With supporting text below as a natural lead-in to additional
                  content.
                </p>
                <a href="#" class="mx-2 align-self-center">Go somewhere</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- ***** next parallax ***** -->

    <div class="background-parallax" id="parallax-img-2">
      <div class="container-fluid background-parallax__content">
        <div class="row justify-content-xs-center justify-content-lg-around">
          <div class="col-lg-5 p-5">
            <img
              class="background-parallax__content__img"
              src="../assets/img/home/dog_vector2.svg"
              alt="vector_dog2"
            />
          </div>
          <div
            class="col-lg-4 d-flex flex-column justify-content-center align-items-center"
          >
            <h3 class="display-4">Todo lo que necesite tu mascota</h3>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Necessitatibus, sequi maiores similique error, commodi cum
              accusamus voluptates corrupti quam blanditiis illum asperiores
              eligendi consequuntur tenetur eius pariatur illo. Nulla, a?
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="dogs-programs">
    <h3 class="display-4">Te ofrecemos lo mejor</h3>
    <div class="container-fluid">
      <div class="row">
        <div
          class="col-lg-4 order-2 order-lg-1 d-flex flex-column aling-items-center justify-content-around"
        >
          <div class="dog-program">
            <div class="dog-program__content text-end">
              <h3 class="display-6 text-end">Group Training</h3>
              <p class="text-end">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum
                tenetur
              </p>
            </div>
            <img
              src="../assets/img/program1.jpg"
              alt="icon-dog"
              class="dog-program__img"
            />
          </div>
          <div class="dog-program">
            <div class="dog-program__content text-end">
              <h3 class="display-6 text-end">Food</h3>
              <p class="text-end">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum
                tenetur
              </p>
            </div>
            <img
              src="../assets/img/program2.jpg"
              alt="icon-dog"
              class="dog-program__img"
            />
          </div>
          <div class="dog-program">
            <div class="dog-program__content text-end">
              <h3 class="display-6 text-end">Veterinaty</h3>
              <p class="text-end">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum
                tenetur
              </p>
            </div>
            <img
              src="../assets/img/program3.jpg"
              alt="icon-dog"
              class="dog-program__img"
            />
          </div>
        </div>
        <div
          class="col-lg-4 order-1 order-lg-2 d-flex aling-items-center justify-content-center"
        >
          <img
            id="dog-img"
            src="../assets/img/background-dog-white.jpg"
            alt="dog-big"
          />
        </div>
        <div
          class="col-lg-4 order-3 order-lg-3 d-flex flex-column aling-items-center justify-content-around"
        >
          <div class="dog-program">
            <img
              src="../assets/img/program4.jpg"
              alt="icon-dog"
              class="dog-program__img"
            />
            <div class="dog-program__content">
              <h3 class="display-6 text-start">Group Toys</h3>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum
                tenetur
              </p>
            </div>
          </div>
          <div class="dog-program">
            <img
              src="../assets/img/program5.jpg"
              alt="icon-dog"
              class="dog-program__img"
            />
            <div class="dog-program__content">
              <h3 class="display-6 text-start">Events</h3>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum
                tenetur
              </p>
            </div>
          </div>
          <div class="dog-program">
            <img
              src="../assets/img/program6.jpg"
              alt="icon-dog"
              class="dog-program__img"
            />
            <div class="dog-program__content">
              <h3 class="display-6 text-start">Advises</h3>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum
                tenetur
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

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
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

export default {
  name: "Home",
  components: {
    DogCards,
    Header,
    Footer,
    Main,
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  data: function () {
    return {
      slideImages: ["slider1.jpg", "slider2.jpg", "slider3.jpg", "slider4.jpg"],
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/scss/_constants.scss";

// *****************************
// * Carrousel Section

.carousel {
  width: 600px;
  margin-bottom: 3rem;
}
.carousel__item {
  // min-height: 50vh;
  width: 100%;
  background-color: transparent;
  color: $white;
  font-size: 20px;
  border-radius: 15px;
  display: flex;
  justify-content: center;
  align-items: center;

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 15px;
  }
}

.carousel__slide {
  padding: 10%;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid $white;
}

@include responsive(large-screen) {
  .carousel {
    width: 80vw;
  }

  .carousel__item {
    min-height: 30vh;
  }
}

// *****************************
// * Parallax sections

.parallax__content {
  min-height: 80vh;
  padding: 10%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  @include button-link;

  h3,
  h5 {
    text-align: center;
    color: $primary;
    font-family: $font-family-subtitle;
  }

  h3 {
    margin-bottom: 1rem;
  }

  p {
    text-align: center;
    color: $primary;
    font-family: $font-family-text;
  }

  .card {
    border: none;
  }

  .card-body {
    background-color: $contrast;
    border-radius: 15px;
    padding: 1rem;
    transition: 0.2s ease-in-out;

    &:hover {
      border: 2.5px solid $primary;
    }
  }
}

.section-parallax {
  // height: 100vh;
  overflow: hidden;
  width: 100vw;
  // overflow-y: auto;
  // perspective: 3px;
}

.background-parallax {
  background-size: cover;
  // background-position: center bottom;
  background-attachment: fixed;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;

  &__content {
    padding: 7%;
    text-align: center;

    h3 {
      color: $secondary;
      font-family: $font-family-subtitle;
      text-shadow: 3px 5px 2px $shadow;

      padding: 2rem 0;
    }
    p {
      color: $white;
      font-family: $font-family-text;
    }

    &__img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }
}

#parallax-img-1 {
  background-image: url("~@/assets/img/home/dog-section1.jpg");
}

#parallax-img-2 {
  background-image: url("~@/assets/img/home/dog-section2.jpg");
}

@include responsive(large-screen) {
  .background-parallax {
    background-position: center bottom;
    &__content {
      &__img {
        width: 80%;
        height: 80%;
      }
    }
  }
}

// *****************************
// * Dogs Section

.dogs-programs {
  width: 100vw;
  padding: 4rem;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;

  h3 {
    width: 100%;
    color: $black;
    text-align: center;
    padding-top: 0rem;
    padding-bottom: 2.5rem;
    font-family: $font-family-subtitle;
  }

  #dog-img {
    width: auto;
    height: auto;
    object-fit: contain;
  }

  .dog-program {
    display: flex;
    align-items: center;
    &__content {
      text-align: left;
      padding-bottom: 1.5rem;

      h3 {
        font-family: $font-family-subtitle;
        color: $primary;
      }

      p {
        color: $primary;
        font-family: $font-family-text;
      }
    }

    &__img {
      width: 120px;
      height: 120px;
      padding: 1.3rem 1.4rem;
    }
  }
}

@include responsive(large-screen) {
  .dogs-programs {
    #dog-img {
      width: 76vw;
      height: auto;
    }

    .dog-program {
      display: flex;
      flex-direction: column;
      align-items: center;
      &__content {
        order: 2;

        h3,
        p {
          text-align: center !important;
          padding: 1.2rem;
        }
      }

      &__img {
        order: 1;
      }
    }
  }
}
</style>
