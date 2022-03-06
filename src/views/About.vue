<template>
  <Header />

  <Main
    title="Conoce más sobre nosotros"
    subtitle="Descubre lo que tu mascota quiere"
    imgBackground="about/about_banner.jpg"
  />

  <section class="section-parallax">
    <!-- ***** next parallax ***** -->

    <div class="parallax__content">
      <h3 class="display-3">Nuestros Empleados</h3>
      <div class="container">
        <div
          class="row gy-5 d-flex align-items-center justify-content-center justify-content-lg-around"
        >
          <div class="col-lg-3">
            <div class="card my-5">
              <div class="card-body d-flex flex-column align-items-center">
                <img src="../assets/img/about/employeer1.jpg" alt="employee1" />
                <h5 class="card-title p-2">Special Manager</h5>
                <p class="card-text px-2 py-3">
                  With supporting text below as a natural lead-in to additional
                  content.
                </p>
                <a href="#" class="mx-2 align-self-center">Conocer</a>
              </div>
            </div>
          </div>
          <div class="col-lg-3">
            <div class="card my-5">
              <div class="card-body d-flex flex-column align-items-center">
                <img src="../assets/img/about/employeer2.jpg" alt="employee2" />

                <h5 class="card-title p-2">Project Director</h5>
                <p class="card-text px-2 py-3">
                  With supporting text below as a natural lead-in to additional
                  content.
                </p>
                <a href="#" class="mx-2 align-self-center">Conocer</a>
              </div>
            </div>
          </div>
          <div class="col-lg-3">
            <div class="card my-5">
              <div class="card-body d-flex flex-column align-items-center">
                <img src="../assets/img/about/employeer3.jpg" alt="employee3" />

                <h5 class="card-title p-2">CEO Director</h5>
                <p class="card-text px-2 py-3">
                  With supporting text below as a natural lead-in to additional
                  content.
                </p>
                <a href="#" class="mx-2 align-self-center">Conocer</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- ***** next parallax ***** -->

    <div
      class="background-parallax d-flex justify-content-center align-items-center"
      id="parallax-img-1"
    >
      <div class="container-fluid background-parallax__content">
        <div class="row justify-content-xs-center justify-content-lg-around">
          <div
            class="col-lg-4 d-flex flex-column justify-content-center align-items-center"
          >
            <h3 class="display-4">Desde nuestro nacimiento en 2008</h3>
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
              src="../assets/img/about/section-parallex1.svg"
              alt="vector_dog1"
            />
          </div>
        </div>
      </div>
    </div>

    <!-- ***** next parallax ***** -->

    <!-- :sources Es para cambiar de videos en responsive -->
    <!-- 
      :sources="[
        {
          src: require(`@/assets/videos/dog-video2.mp4`),
          res: 900,
          autoplay: true,
        },
        {
          src: require(`@/assets/videos/dog-video3.mp4`),
          res: 638,
          autoplay: true,
        },
      ]"
     -->
    <VideoBackground
      :src="require(`@/assets/videos/dog-video.mp4`)"
      overlay="linear-gradient(180deg,#2a4ae430,#fb949e6b)"
      class="background-video"
    >
      <div class="parallax__content parallax__content--video">
        <h3 class="display-4">Vive una experiencía única con tu mascota</h3>

        <div class="container-fluid">
          <div class="row">
            <div
              class="col-lg-4 d-flex align-items-center justify-content-center my-5 px-4"
            >
              <div class="tarjeta-viaje">
                <div class="img-viaje">
                  <img
                    src="./../assets/img/about/employeer1.jpg"
                    alt="video-img-1"
                  />
                </div>

                <div class="contenido-viaje">
                  <h3>Amor</h3>
                  <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Incidunt aliquam assumenda id commodi, accusamus quas
                    possimus? Sit vel porro.
                  </p>
                </div>
              </div>
            </div>
            <div
              class="col-lg-4 d-flex align-items-center justify-content-center my-5 px-4"
            >
              <div class="tarjeta-viaje">
                <div class="img-viaje">
                  <img
                    src="./../assets/img/about/employeer1.jpg"
                    alt="video-img-2"
                  />
                </div>

                <div class="contenido-viaje">
                  <h3>honestidad</h3>
                  <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Incidunt aliquam assumenda id commodi, accusamus quas
                    possimus? Sit vel porro.
                  </p>
                </div>
              </div>
            </div>
            <div
              class="col-lg-4 d-flex align-items-center justify-content-center my-5 px-4"
            >
              <div class="tarjeta-viaje">
                <div class="img-viaje">
                  <img
                    src="./../assets/img/about/employeer1.jpg"
                    alt="video-img-3"
                  />
                </div>

                <div class="contenido-viaje">
                  <h3>Confianza</h3>
                  <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Incidunt aliquam assumenda id commodi, accusamus quas
                    possimus? Sit vel porro.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </VideoBackground>

    <!-- ***** next parallax ***** -->

    <div
      class="background-parallax d-flex justify-content-center align-items-center"
      id="parallax-img-2"
    >
      <div class="container-fluid background-parallax__content">
        <div class="row justify-content-xs-center justify-content-lg-around">
          <div class="col-lg-5 p-lg-5">
            <img
              class="background-parallax__content__img"
              src="../assets/img/about/section-parallex2.svg"
              alt="vector_dog2"
            />
          </div>
          <div
            class="col-lg-4 d-flex flex-column justify-content-center align-items-center"
          >
            <h3 class="display-4">Nuestra misión nos acerca a tí</h3>
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

  <Footer />
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import Main from "@/components/Main.vue";
import VideoBackground from "vue-responsive-video-background-player";

export default {
  name: "Home",
  components: {
    Header,
    Footer,
    Main,
    VideoBackground,
  },
};
</script>

<style scoped lang="scss">
@import "@/scss/_constants.scss";

// *****************************
// * Parallax sections

.background-video {
  min-height: 110vh;
}

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
    margin-bottom: 3rem;
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
    border-radius: 15px;
    padding: 1rem;
    border: 1.5px solid $primary;
    transition: 0.1s ease-in-out;

    img {
      border-radius: 50%;
      object-fit: cover;
      width: 50%;
      height: 50%;
      margin-bottom: 2rem;
    }

    &:hover {
      border: 3px solid $primary;
    }
  }

  // * Section video
  &--video {
    // height: 800px;
    padding: 5rem 0rem;
    h3 {
      color: $secondary;
      font-family: $font-family-subtitle;
      text-shadow: 3px 5px 2px $shadow;
    }
  }
}

@include responsive(large-screen) {
  .background-video {
    min-height: 180vh;
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
  align-items: flex-start;
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
  background-image: url("~@/assets/img/about/dog-section1-about.jpg");
}

#parallax-img-2 {
  background-image: url("~@/assets/img/about/dog-section2-about.jpg");
}

@include responsive(large-screen) {
  .background-parallax {
    background-position: center bottom;
    height: unset;
    padding-bottom: 3rem;
    &__content {
      &__img {
        width: 80%;
        height: 80%;
      }
    }
  }
}

// *******************

.tarjeta-viaje {
  position: relative;
  max-width: 300px;
  height: 190px;
  background: $tertiary;
  display: flex;
  flex-direction: column;
  box-shadow: 0 5px 35px $shadow;
  transition: 0.3s ease-in-out;
  border-radius: 11px;

  &:hover {
    height: 450px;

    .img-viaje img {
      // opacity: 100%;
    }

    .contenido-viaje {
      visibility: visible;
      // opacity: 1;
      margin-top: -20px;
      transition-delay: 0.3s;

      p {
        color: $white;
      }
    }
  }

  .img-viaje {
    position: relative;
    width: 85%;
    height: 310px;
    top: -40px;
    left: 20px;
    z-index: 1;

    img {
      border-radius: 6px;
      // opacity: 92%;
      height: 100%;
      width: 100%;
      box-shadow: 10px 15px 25px rgba(0, 0, 0, 0.707);
    }
  }

  .contenido-viaje {
    position: relative;
    padding: 1.5rem 15px;
    text-align: center;
    color: #111;
    visibility: hidden;
    // opacity: 1;
    transition: 0.3s ease-in-out;

    h3 {
      margin-bottom: 1rem;
    }
  }
}
</style>
