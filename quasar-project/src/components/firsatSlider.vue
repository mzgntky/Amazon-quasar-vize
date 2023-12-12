<template>
  <div class="q-pa-md row items-start q-gutter-md">
    <h5>Öne çıkan fırsat ve mağazalar</h5>
    <div class="product-carousel" style="background-color: rgb(255, 253, 253)">
      <div class="product-card" v-for="product in products" :key="product.id">
        <img :src="product.image" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

interface Product {
  id: number;
  image: string;
}

import product1 from 'src/static/cm1.jpg';
import product2 from 'src/static/cm2.jpg';
import product3 from 'src/static/cm3.jpg';
import product4 from 'src/static/cm4.jpg';

export default defineComponent({
  data() {
    return {
      products: [
        { id: 1, image: product1 },
        { id: 2, image: product2 },
        { id: 3, image: product3 },
        { id: 4, image: product4 },
        { id: 5, image: product2 },
        { id: 6, image: product3 },
        { id: 7, image: product1 },
        { id: 8, image: product4 },
        { id: 9, image: product3 },
        { id: 10, image: product1 },
        { id: 11, image: product4 },
        { id: 12, image: product3 },
        // ... diğer ürünler ...
      ] as Product[],
    };
  },
});
</script>

<style scoped>
/* Carousel Container ve Card stilleri */
.product-carousel {
  display: flex;
  overflow-x: auto;
}

.product-card {
  min-width: 200px;
  margin-right: 20px;
  border: 1px solid #ddd;
  padding: 10px;
  border-radius: 5px;
}

.product-card img {
  max-width: 100%;
  height: auto;
  border-radius: 5px;
}

.product-info {
  text-align: center;
}

.product-name {
  font-size: 16px;
  margin-bottom: 5px;
}

.product-price {
  font-size: 14px;
  color: #007bff;
}
</style>
