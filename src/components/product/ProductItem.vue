<template>
  <v-card elevation="0" class="border">
    <v-img :src="productItem.image" :height="`${height}px`"></v-img>
    <v-card-item class="pb-4 bg-ash">
      <div class="text-subtitle-1 font-weight-bold secondary-font">
        {{ productItem.name }}
      </div>
      <div class="text-subtitle-2 secondary-font">{{ productItem.model }}</div>
      <div class="sell-content mt-2">
        <div class="text-h6 secondary-font font-weight-bold">
          {{ productItem.price }} euro
        </div>

       
      </div>
    </v-card-item>
  </v-card>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  productItem: {
    type: Object,
    required: true,
  },
  height: {
    type: [String, Number], 
    default: 300, 
  },
});
</script>

<style lang="scss" scoped>
.bg-ash {
  background-color: #f3f3f3;
}
</style>
