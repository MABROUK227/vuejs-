<template>
  <div class="home-feature">
    <v-container fluid>
      <v-row>
        <v-col cols="5">
          <div class="text-h2 font-weight-black">
            Transformez votre espace de vie avec un style qui dure
          </div>
          <div class="text-h5 mt-4">
            Organisez chaque espace avec nos collections de meubles intemporelles
          </div>
          <ul class="mt-5">
            <li>
              <span class="mdi mdi-check"></span> À eleifend mattis ligula, porta finibus
              urna gvida at.
            </li>
            <li>
              <span class="mdi mdi-check"></span> Kenean vehicula sodales arcu non mattis.
            </li>
            <li>
              <span class="mdi mdi-check"></span> Ginteger dapibus ac dui pretium blanss
              aptent.
            </li>
          </ul>
        </v-col>
        <v-col cols="7">
          <div class="feature-image">
            <v-img src="../../assets/images/feature/d.png"></v-img>
          </div>
          <div class="feature-image-slide mt-5">
            <swiper
              :slidesPerView="3"
              :spaceBetween="20"
              :navigation="true"
              :modules="modules"
              class="mySwiper"
            >
              <swiper-slide
                v-for="(product, index) in showProduct"
                :key="index"
                class="pb-1"
              >
                <ProductShowItem :show-item="product" />
              </swiper-slide>
            </swiper>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";

// Importer les styles de Swiper
import "swiper/css";
import "swiper/css/navigation";

// importer les modules requis
import { Navigation } from "swiper/modules";
import { ref } from "vue";
import ProductShowItem from "../product/ProductShowItem.vue";

// Définir les modules
const modules = [Navigation];

const showProduct = ref([
  {
    name: "CHAIR UNIQUE SIMPLE",
    image: "src/assets/images/product/chair.png",
    model: "SDC-227-9-1-66",
  },
  {
    name: "SIÈGE EN CUIR MOELLEUX",
    image: "src/assets/images/product/leather-soft.png",
    model: "SDC-227-9-1-66",
  },
  {
    name: "CHAIR UNIQUE MOELLEUSE",
    image: "src/assets/images/product/soft-chair.png",
    model: "SDC-227-9-1-66",
  },
  {
    name: "CANAPÉ DOUBLE - POMPEI",
    image: "src/assets/images/product/brown-coution.png",
    model: "SDC-227-9-1-66 (REXINE)",
  },
  {
    name: "CHAIR CANAPÉ - POMPEI",
    image: "src/assets/images/product/purple-chair.png",
    model: "SDC-227-9-1-66",
  },
  {
    name: "ENSEMBLE CANAPÉ AVEC TABLE À THÉ",
    image: "src/assets/images/product/sofaset.png",
    model: "SDC-118-9-1-66",
    price: "16 000",
  },
]);
</script>

<style scoped lang="scss">
.home-feature {
  background-color: rgba(229, 228, 228, 0.5);
  padding: 100px 0;
  margin: 70px 0 70px 0;
}
</style>
