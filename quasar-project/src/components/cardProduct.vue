<template>
  <div class="q-pa-md row items-start q-gutter-md">
    <h5>Ürünler</h5>
    <div class="product-carousel" style="background-color: rgb(255, 255, 255)">
      <div class="product-card" v-for="product in products" :key="product.id">
        <img
          :src="product.image"
          :alt="product.name"
          style="max-height: 100px"
        />
        <div class="product-info">
          <p class="product-name">{{ product.name }}</p>
          <p class="product-price">{{ product.price }} TL</p>
          <q-row>
            <q-col>
              <router-link to="product/1">
                <q-btn size="sm" text-color="black">Ürünü İncele</q-btn>
              </router-link>
            </q-col>
            <q-col>
              <router-link to="basket">
                <q-btn size="sm" text-color="black">Sepete Ekle</q-btn>
              </router-link>
            </q-col>
          </q-row>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

interface Product {
  id: number;
  name: string;
  price: number;
  image: string;
}

import product1 from 'src/static/p1.jpg';
import product2 from 'src/static/p2.jpg';
import product3 from 'src/static/p3.jpg';
import product4 from 'src/static/p4.jpg';
import product5 from 'src/static/p5.jpg';
import product6 from 'src/static/p6.jpg';

export default defineComponent({
  data() {
    return {
      products: [
        { id: 1, name: 'Kulaklık', price: 800, image: product1 },
        { id: 2, name: 'Monitör', price: 2000, image: product2 },
        { id: 3, name: 'Kahve Makinası', price: 500, image: product3 },
        { id: 4, name: 'Avize', price: 700, image: product4 },
        { id: 5, name: 'Ayakkabı', price: 200, image: product5 },
        { id: 6, name: 'Kitap', price: 70, image: product6 },
        { id: 7, name: 'Kulaklık', price: 800, image: product1 },
        { id: 8, name: 'Avize', price: 700, image: product4 },
        { id: 9, name: 'Kahve Makinası', price: 500, image: product3 },
        { id: 10, name: 'Kitap', price: 70, image: product6 },
        { id: 11, name: 'Avize', price: 700, image: product4 },
        { id: 12, name: 'Kahve Makinası', price: 500, image: product3 },
        // ... diğer ürünler ...
      ] as Product[],
    };
  },
});
</script>

<style scoped>
@import '../css/bootstrap.css';
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
