<template>
  <footer>
    <div class="container text-center text-md-left">
      <div class="row text-center text-md-left">
        <div class="col-md-3 mx-auto mt-3">
          <h5 class="text-uppercase mb-4 font-weight-bold">Poppy inc.</h5>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptatum
            nulla libero similique fugiat. Eaque quis, adipisci repellat
          </p>
        </div>
        <div class="col-md-3 mx-auto mt-3">
          <h5 class="text-uppercase mb-4 font-weight-bold">Servicios</h5>
          <p>
            <a href="#" class="text-white"> Adopción </a>
          </p>
          <p>
            <a href="#" class="text-white"> Productos </a>
          </p>
          <p>
            <a href="#" class="text-white"> Cuidador </a>
          </p>
          <p>
            <a href="#" class="text-white"> Veterinario </a>
          </p>
        </div>
        <div class="col-md-3 mx-auto mt-3">
          <h5 class="text-uppercase mb-4 font-weight-bold">
            Enlaces de interés
          </h5>
          <p>
            <a href="#" class="text-white"> Nuestros Clientes </a>
          </p>
          <p>
            <a href="#" class="text-white"> Dirección </a>
          </p>
          <p>
            <a href="#" class="text-white"> Proyectos </a>
          </p>
          <p>
            <a href="#" class="text-white"> Contacto </a>
          </p>
        </div>

        <div class="col-md-3 mx-auto mt-3">
          <h5 class="text-uppercase mb-4 font-weight-bold">Contacto</h5>
          <p>
            <a href="#" class="text-white">
              <i class="bi bi-signpost-2"></i>
              <span>Palma de Mallorca </span>
            </a>
          </p>
          <p>
            <a href="#" class="text-white">
              <i class="bi bi-envelope-check"></i>
              <span>puppies@gmail.com </span>
            </a>
          </p>
          <p>
            <a href="#" class="text-white">
              <i class="bi bi-telephone"></i>
              <span>+36 66666666 </span>
            </a>
          </p>
        </div>
      </div>

      <hr class="mb-4" />

      <div class="row align-items center">
        <div
          class="col-md-7 d-flex align-items-center justify-content-center pb-3"
        >
          <p>
            Copyright @2022 by:
            <strong> Puppies Inc. </strong>
          </p>
        </div>

        <div class="col-md-4">
          <div class="text-center text-md-right">
            <ul class="list-unstyled list-inline d-flex justify-content-evenly">
              <li class="list-inline-item">
                <i class="bi bi-facebook social-media"></i>
              </li>
              <li class="list-inline-item">
                <i class="bi bi-twitter social-media"></i>
              </li>
              <li class="list-inline-item">
                <i class="bi bi-instagram social-media"></i>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
<script>
import { useRouter } from "vue-router";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  computed: {
    currentRouteName() {
      return useRouter().currentRoute.value.name;
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/scss/_constants.scss";

footer {
  // background: transparent !important;
  background: $tertiary;
  padding: 2rem 2.5rem;
  width: 100vw;
  color: $white;

  // &__logo {
  //   width: 25rem;
  //   img {
  //     margin-right: 2rem;
  //     width: 80px;
  //     height: 130px;
  //   }

  //   h2 {
  //     font-family: $font-family-title;
  //     color: $secondary;
  //   }
  // }

  // @include responsive(medium-screen) {
  //   &__logo {
  //     width: 35vw;
  //   }
  // }

  // @include responsive(small-screen) {
  //   padding: 1.5rem;

  //   &__logo {
  //     width: 45vw;

  //     img {
  //       margin-right: 1rem;
  //       width: 60px !important;
  //       height: 110px !important;
  //     }
  //   }
  // }

  h5 {
    color: $secondary;
    font-family: $font-family-subtitle;
  }

  a {
    font-family: $font-family-text;
    text-decoration: none;
    position: relative;

    .bi {
      margin-top: auto;
    }

    &::after {
      position: absolute;
      bottom: -0.4rem;
      left: 0;
      width: 100%;
      background-color: $secondary;
      height: 0.1em;
      content: "";
      opacity: 0;
      transition: opacity 300ms, transform 300ms;
    }

    &:hover::after,
    &:focus::after {
      opacity: 1;
      transform: translate3d(0, 0.2em, 0);
    }
  }

  p {
    font-family: $font-family-text;
  }

  .bi {
    font-size: 2rem;
    padding-right: 1rem;
  }

  strong {
    color: $secondary;
    font-family: $font-family-text;
  }

  .social-media {
    font-size: 2.2rem;
    color: $white;
    border: 2px solid $secondary;
    padding-right: 0rem;
    border-radius: 50%;
    padding: 0.6rem;

    &:hover {
      transition: 0.5s ease-in-out;
      background-color: $secondary;
    }
  }
}

// .offcanvas-end {
//   width: 100% !important;
// }

// .disabled {
//   opacity: 0.5;
//   pointer-events: none;
// }
</style>
