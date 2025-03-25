<template>
  <div class="conteneur-categorie-laterale"></div>
  <v-card width="260" min-height="600" elevation="2" rounded="lg">
    <v-list select-strategy="classic">
      <v-list-subheader>Liste des catégories</v-list-subheader>
      <v-divider class="mb-4"></v-divider>
      <div v-for="(item, index) in categories" :key="index">
        <SideCategoryItem :category-item="item" />
      </div>
    </v-list>
  </v-card>
</template>

<script setup>
import { ref } from "vue";
import SideCategoryItem from "./SideCategoryItem.vue";

const categories = ref([
  {
    title: "Salon",
    itemQuantity: "78 Articles",
  },
  {
    title: "Chambre",
    itemQuantity: "120 Articles",
  },
  {
    title: "Bureau",
    itemQuantity: "57 Articles",
  },
  {
    title: "Bureau à domicile",
    itemQuantity: "90 Articles",
  },
  {
    title: "Éclairage",
    itemQuantity: "70 Articles",
  },
  {
    title: "Cuisine",
    itemQuantity: "80 Articles",
  },
  {
    title: "Restaurant",
    itemQuantity: "190 Articles",
  },
]);
</script>

<style lang="scss" scoped></style>
