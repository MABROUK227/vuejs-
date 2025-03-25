<template>
  <v-container class="hero-section d-flex align-center h-screen">
    <div class="hero-lamp position-absolute left-60 zIndex-2">
      <v-img src="../../assets/images/hero/lamp.svg" height="240" width="200"></v-img>
    </div>
    <v-row align="center">
      <v-col cols="6">
        <v-card elevation="0">
          <v-card-item>
            <div class="text-h2 font-weight-black">
              Nous aidons
              <span class="position-relative"
                >À créer
                <v-img
                  width="240"
                  src="../../assets/images/hero/line.svg"
                  class="position-absolute right-0"
                ></v-img>
              </span>
              <br />
              Vos espaces de rêve<span class="secondary-color">.</span>
            </div>
            <div class="text-body-1 font-weight-regular mt-4">
              Nous recherchons, créons et construisons des lieux de travail en
              fusionnant design, technologie et innovation. Laissez notre équipe
              d'architecture intérieure vous aider à créer une meilleure entreprise.
            </div>
            <v-btn
              append-icon="mdi-cart"
              variant="flat"
              color="primary"
              rounded="lg"
              class="mt-4"
            >
              Achetez maintenant
            </v-btn>
          </v-card-item>
        </v-card>
      </v-col>
      <v-col cols="6">
        <div class="hero-img position-relative zIndex-2">
          <v-img
            src="../../assets/images/product/brown-coution.png "
            class="mx-auto"
            max-height="400"
          >
          </v-img>
        </div>

        <div class="hero-img-bg"></div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup></script>

<style scoped>
.hero-section {
  position: relative;
}
.hero-lamp {
  top: -85px;
  left: 170px;
}
.hero-img-bg {
  height: 450px;
  width: 450px;
  position: absolute;
  right: 0;
  bottom: 50px;
  filter: blur(45px);
  transform: translateZ(0);
  z-index: 1;
  background: radial-gradient(#ffbc11b7, rgba(1, 65, 255, 0));
}
</style>
