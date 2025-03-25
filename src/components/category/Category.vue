<template>
  <v-container>
    <div class="liste-categories">
      <swiper
        :slidesPerView="6"
        :spaceBetween="20"
        :navigation="true"
        :modules="modules"
        class="mySwiper"
      >
        <swiper-slide v-for="(item, index) in categories" :key="index" class="pb-1">
          <CategoryItem :category-item="item" />
        </swiper-slide>
      </swiper>
    </div>
  </v-container>
</template>

<script setup>
import { ref } from "vue";
import CategoryItem from "./CategoryItem.vue";

import { Swiper, SwiperSlide } from "swiper/vue";

// Importation des styles Swiper
import "swiper/css";
import "swiper/css/navigation";

// Importation des modules requis
import { Navigation } from "swiper/modules";

// Définition des modules
const modules = [Navigation];

const categories = ref([
  {
    title: "Salon",
    itemQuantity: "78 Articles",
    image: "src/assets/images/category/living.png",
  },
  {
    title: "Chambre",
    itemQuantity: "120 Articles",
    image: "src/assets/images/category/bathroom.png",
  },
  {
    title: "Bureau",
    itemQuantity: "57 Articles",
    image: "src/assets/images/category/office-desk.png",
  },
  {
    title: "Bureau à domicile",
    itemQuantity: "90 Articles",
    image: "src/assets/images/category/meeting-room.png",
  },
  {
    title: "Éclairage",
    itemQuantity: "70 Articles",
    image: "src/assets/images/category/lamp.png",
  },
  {
    title: "Cuisine",
    itemQuantity: "80 Articles",
    image: "src/assets/images/category/kitchen.png",
  },
  {
    title: "Restaurant",
    itemQuantity: "190 Articles",
    image: "src/assets/images/category/restaurant.png",
  },
]);
</script>

<style lang="scss" scoped></style>
