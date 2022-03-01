<template>
  <header>
    <nav
      :class="{ changeColorScroll: scrollPosition > 450 }"
      class="navbar fixed-top navbar-expand-md navbar-light"
      id="navbar"
    >
      <div class="container-fluid">
        <router-link
          class="navbar-brand d-flex flex-row justify-content-center align-items-center"
          id="navbar__logo"
          :to="{ name: 'Home' }"
        >
          <img src="../assets/img/dog_logo.svg" alt="" class="" />
          <h2 class="display-4">Puppy</h2>
        </router-link>

        <button
          id="navbar__burguer"
          class="navbar-toggler custom-toggler"
          type="button"
          data-bs-toggle="offcanvas"
          data-bs-target="#offcanvasNavbar"
          aria-controls="offcanvasNavbar"
        >
          <i class="bi bi-list"></i>
        </button>
        <div
          class="offcanvas offcanvas-end"
          tabindex="-1"
          id="offcanvasNavbar"
          aria-labelledby="offcanvasNavbarLabel"
        >
          <div class="offcanvas-header">
            <h5 class="offcanvas-title display-4" id="offcanvasNavbarLabel">
              Puppy
            </h5>
            <button
              type="button"
              id="navbar__btn-close"
              data-bs-dismiss="offcanvas"
              aria-label="Close"
            >
              <i class="bi bi-x-lg"></i>
            </button>
          </div>
          <div class="offcanvas-body">
            <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
              <li class="nav-item">
                <router-link
                  :class="{
                    disabled: currentRouteName === 'Home' ? true : false,
                  }"
                  class="nav-link"
                  :to="{ name: 'Home' }"
                  >Home</router-link
                >
              </li>
              <li class="nav-item">
                <router-link
                  :class="{
                    disabled: currentRouteName === 'About' ? true : false,
                  }"
                  class="nav-link"
                  :to="{ name: 'About' }"
                  >About</router-link
                >
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>
<script>
import { useRouter } from "vue-router";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data: function () {
    return {
      scrollPosition: null,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  },
  computed: {
    currentRouteName() {
      return useRouter().currentRoute.value.name;
    },
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY;
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/scss/_constants.scss";

@mixin link-animation($bottom, $left, $width) {
  a:hover {
    transform: scale(1.1);
    transition: 0.3s;
  }

  a::after {
    position: absolute;
    bottom: $bottom;
    left: $left;
    width: $width;
    background-color: $secondary;
    height: 0.1em;
    content: "";
    opacity: 0;
    transition: opacity 300ms, transform 300ms;
  }

  a:hover::after,
  a:focus::after {
    opacity: 1;
    transform: translate3d(0, 0.2em, 0);
  }
}

.changeColorScroll {
  background: $primary !important;
  transition: 1s ease-in-out;
}

#navbar {
  background: transparent;
  transition: 1s ease-in-out;
  padding: 0rem;
  height: 140px;

  &__logo {
    width: 25rem;
    img {
      margin-right: 2rem;
      width: 80px;
      height: 130px;
    }

    h2 {
      font-family: $font-family-title;
      color: $secondary;
      text-shadow: 3px 5px 2px $shadow;
      transition: transform 0.2s;

      &:hover {
        transform: scale(1.2);
        transition: 0.3s;
      }
    }
  }

  &__burguer {
    border-color: none !important;
    border: none !important;
    color: none !important;
    background-color: transparent;

    &:focus {
      border-color: none !important;
      border: none !important;
      color: none !important;
      box-shadow: none !important;
    }

    .bi-list {
      font-size: 5rem;
      color: $secondary;
    }
  }

  // OffCanvas

  .offcanvas {
    // background: $tertiary;
    padding: 1.5rem;
  }

  .offcanvas-end {
    width: 100% !important;
  }

  .offcanvas-header {
    height: 15vh;

    h5 {
      font-family: $font-family-title;
      color: $secondary;
    }
  }

  &__btn-close {
    border: none;
    background: transparent;

    .bi-x-lg {
      font-size: 5rem;
      color: $tertiary;
    }
  }

  .show {
    li {
      display: flex;
      justify-content: center;
    }

    a {
      width: 290px;
      text-align: center;
    }
    @include link-animation(6px, 34%, 55%);
    a::after {
      width: 55% !important;
    }
  }

  // Enlaces

  a {
    font-family: $font-family-text;
    color: $secondary;
    padding: 1rem 2rem;
    font-size: 2rem;
    text-shadow: 3px 2px 2px $shadow;
    position: relative;

    &:last-of-type {
      padding-right: 0rem;
    }
  }
  .nav-item {
    a {
      transition: transform 0.2s;
    }
    @include link-animation(14px, 30%, 70%);
  }

  .disabled {
    opacity: 0.5;
    pointer-events: none;
  }

  @include responsive(medium-screen) {
    padding: 0 1.2rem;
    height: 150px;
    &__logo {
      width: 35vw;
      padding: 0rem !important;
    }
  }

  @include responsive(small-screen) {
    height: 130px;
    padding: 0 0.5rem;


    &__logo {
      width: 45vw;

      img {
        margin-right: 1rem;
        width: 60px !important;
        height: 110px !important;
      }
    }
  }

  @include responsive(extra-small) {
    padding: 0rem 0.5rem;
    height: 110px;

    &__logo {
      width: 45vw;

      img {
        margin-right: 1rem;
        width: 40px !important;
        height: 90px !important;
      }
    }

    &__burguer {
      .bi-list {
        font-size: 3.5rem;
      }
    }

    &__btn-close {
      .bi-x-lg {
        font-size: 3.5rem;
      }
    }
  }
}
</style>
