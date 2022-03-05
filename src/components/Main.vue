<template>
  <main :style="backgroundStyles">
    <div class="first-panel container-fluid">
      <div class="row justify-content-center justify-content-xxl-end">
        <div
          class="col-8 col-xxl-4 d-flex flex-column align-items-center text-center"
        >
          <h1 class="display-3">
            {{ title }}
          </h1>

          <h2 class="display-6">
            {{ subtitle }}
          </h2>
          <img
            v-if="imgSrc"
            :src="require(`@/assets/img/${imgSrc}`)"
            class="index-presentation"
            :alt="title"
          />
        </div>
      </div>
    </div>
  </main>
</template>
<script>
export default {
  name: "Main",
  props: {
    title: String,
    subtitle: String,
    imgSrc: String,
    imgBackground: String,
  },
  computed: {
    backgroundStyles() {
      return `background-image: url("${require("@/assets/img/" +
        this.imgBackground)}");
        background-repeat: no-repeat;
        background-position: left center;
        background-size: cover;
        `;
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/scss/_constants.scss";

/** BACKGROUND GIF */
main {
  height: 100vh !important;
  width: 100vw !important;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  color: $white;
  // background: red;

  img {
    object-fit: cover;
    width: 100px !important;
    height: 100px !important;
  }
}
.first-panel {
  padding: 0rem 3rem;
  // height: 75vh;
}

.first-panel h1 {
  font-family: $font-family-title;
  color: $secondary;
}
.first-panel h2 {
  font-family: $font-family-subtitle;
  color: $white;
  padding-top: 2rem;
}

/** Imagenes que acompañan a la presentación de index.html */
.index-presentation {
  height: auto;
  width: 370px;
}

@include responsive(medium-screen) {
}

@include responsive(small-screen) {
}

@include responsive(extra-small) {
}
</style>
