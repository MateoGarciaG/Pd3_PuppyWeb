<template>
  <Header />

  <Main
    title="Bienvenidos al mundo puppy"
    subtitle="Conocenos!"
    imgBackground="home/home_banner.jpg"
  />

  <section>
    <div class="container">
      <div class="row">
        <div class="col">Column</div>
        <div class="col">Column</div>
        <div class="col">Column</div>
      </div>
    </div>
  </section>

  <article>
    <div class="container">
      <div class="row">
        <div class="col">Column</div>
        <div class="col">Column</div>
        <div class="col">Column</div>
      </div>
    </div>
  </article>

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
              src="../assets/img/program1.png"
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
              src="../assets/img/program2.png"
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
              src="../assets/img/program3.png"
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
              src="../assets/img/program4.png"
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
              src="../assets/img/program5.png"
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
              src="../assets/img/program6.png"
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
