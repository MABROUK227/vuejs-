<template>
  <v-container fluid>
    <div class="section-heading text-center mb-10">
      <div class="text-h3 secondary-font font-weight-bold">Nos Produits Populaires</div>
    </div>
    <swiper
      :slidesPerView="4"
      :spaceBetween="20"
      :navigation="true"
      :modules="modules"
      class="mySwiper"
    >
      <swiper-slide v-for="(product, index) in popularProduct" :key="index" class="pb-1">
        <ProductItem :product-item="product" />
      </swiper-slide>
    </swiper>
  </v-container>
</template>

<script setup>
// Importer les composants Swiper Vue.js
import { Swiper, SwiperSlide } from "swiper/vue";

// Importer les styles Swiper
import "swiper/css";
import "swiper/css/navigation";

// Importer les modules nécessaires
import { Navigation } from "swiper/modules";
import { ref } from "vue";
import ProductItem from "../product/ProductItem.vue";

// Définir les modules
const modules = [Navigation];

const popularProduct = ref([
  {
    name: "CHAISE UNIQUE SIMPLE",
    image: "src/assets/images/product/chair.png",
    model: "SDC-227-9-1-66",
    price: "14 000",
  },
  {
    name: "SIÈGE EN CUIR DOUX",
    image: "src/assets/images/product/leather-soft.png",
    model: "SDC-227-9-1-66",
    price: "11 000",
  },
  {
    name: "CHAIRE UNIQUE DOUCE",
    image: "src/assets/images/product/soft-chair.png",
    model: "SDC-227-9-1-66",
    price: "9 000",
  },
  {
    name: "CANAPÉ DOUBLE - POMPEI",
    image: "src/assets/images/product/brown-coution.png",
    model: "SDC-227-9-1-66 (REXINE)",
    price: "24 000",
  },
  {
    name: "CANAPÉ-CHAIR - POMPEI",
    image: "src/assets/images/product/purple-chair.png",
    model: "SDC-227-9-1-66",
    price: "22 000",
  },
  {
    name: "ENSEMBLE CANAPÉ AVEC TABLE BASSE",
    image: "src/assets/images/product/sofaset.png",
    model: "SDC-118-9-1-66",
    price: "16 000",
  },
  {
    name: "SIÈGE EN CUIR DOUX",
    image: "src/assets/images/product/leather-soft.png",
    model: "SDC-227-9-1-66",
    price: "11 000",
  },
  {
    name: "CHAIRE UNIQUE DOUCE",
    image: "src/assets/images/product/soft-chair.png",
    model: "SDC-227-9-1-66",
    price: "9 000",
  },
  {
    name: "CANAPÉ DOUBLE - POMPEI",
    image: "src/assets/images/product/brown-coution.png",
    model: "SDC-227-9-1-66 (REXINE)",
    price: "24 000",
  },
  {
    name: "CANAPÉ-CHAIR - POMPEI",
    image: "src/assets/images/product/purple-chair.png",
    model: "SDC-227-9-1-66",
    price: "22 000",
  },
  {
    name: "ENSEMBLE CANAPÉ AVEC TABLE BASSE",
    image: "src/assets/images/product/sofaset.png",
    model: "SDC-118-9-1-66",
    price: "16 000",
  },
]);
</script>

<style lang="scss" scoped></style>
