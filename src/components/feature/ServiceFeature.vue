<template>
  <div
    class="service-feature"
    style="background-image: url('src/assets/images/feature/servFeature.webp')"
  >
    <v-container>
      <div class="service-feature-wrapper">
        <div class="text-h3 text-uppercase font-weight-black secondary-font text-center">
          VOUS PAYEZ TROP CHER
        </div>
        <p class="text-center">
          
          Devenez simplement membre du Club et commencez à profiter des avantages de vos achats
        </p>
        <v-row class="mt-10">
          <v-col cols="3" v-for="(item, index) in serviceFeature" :key="index">
            <ServiceFeatureCard :service-feature="item" />
          </v-col>
        </v-row>
      </div>
    </v-container>
  </div>
</template>

<script setup>
import ServiceFeatureCard from "./ServiceFeatureCard.vue";
import { ref } from "vue";

const serviceFeature = ref([
  {
    title: "LIVRAISON RAPIDE",
    detail: "Livraison gratuite sur toutes les commandes supérieures à",
    image: "src/assets/images/feature/shipped.png",
  },
  {
    title: "Politique de retour",
    detail: "Vous pouvez retourner votre achat",
    image: "src/assets/images/feature/purchase.png",
  },
  {
    title: "STOCKS IMPORTANT",
    detail: "Contactez-nous pour toute question",
    image: "src/assets/images/feature/in-stock.png",
  },
  {
    title: "Support Client",
    detail: "Nous sommes là pour vous servir",
    image: "src/assets/images/feature/customer-service.png",
  },
]);
</script>

<style scoped lang="scss">
.service-feature {
  padding: 120px 0;
  width: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  margin: 100px 0;
  position: relative;
  z-index: 1;
  background-attachment: fixed;
  &::after {
    position: absolute;
    content: "";
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: -1;
  }
}
.service-feature-wrapper {
  padding: 80px 40px;
  background-color: #ffffffec;
  border-radius: 26px;
  min-height: 400px;
  max-width: 1000px;
  margin: 0 auto;
}
</style>
