<template>
  <div class="shopping-container">
    <div class="product-list">
      <h2>Ürünler</h2>
      <ul>
        <li v-for="product in products" :key="product.id">
          <img :src="product.image" :alt="product.name" />
          {{ product.name }} - {{ product.price }} TL
          <button @click="addToCart(product)">Sepete Ekle</button>
        </li>
      </ul>
    </div>

    <div class="cart-content">
      <h3>Sepet İçeriği</h3>
      <ul>
        <li v-for="item in cart" :key="item.id">
          <img :src="item.product.image" :alt="item.product.name" />
          {{ item.product.name }} - {{ item.product.price }} TL
          <button @click="removeFromCart(item)">Sepetten Çıkar</button>
        </li>
      </ul>

      <p>Toplam: {{ getTotalPrice() }} TL</p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import p1 from 'src/static/p1.jpg';
import p2 from 'src/static/p4.jpg';
import p3 from 'src/static/p6.jpg';

interface Product {
  id: number;
  name: string;
  price: number;
  image: string;
}

interface CartItem {
  id: number;
  product: Product;
}

export default defineComponent({
  data() {
    return {
      products: [
        { id: 1, name: 'Kulaklık', price: 800, image: p1 },
        { id: 2, name: 'Avize', price: 200, image: p2 },
        { id: 3, name: 'Kitap', price: 70, image: p3 },
      ] as Product[],
      cart: [] as CartItem[],
    };
  },
  methods: {
    addToCart(product: Product) {
      const existingItem = this.cart.find(
        (item) => item.product.id === product.id
      );

      if (existingItem) {
        existingItem.product.price += product.price;
      } else {
        this.cart.push({ id: Date.now(), product });
      }
      alert('Ürün sepete eklendi');
    },
    removeFromCart(item: CartItem) {
      const index = this.cart.indexOf(item);
      if (index !== -1) {
        this.cart.splice(index, 1);
      }
      alert('Ürün sepetten çıkarıldı');
    },
    getTotalPrice() {
      return this.cart.reduce((total, item) => total + item.product.price, 0);
    },
  },
});
</script>
<style scoped>
.shopping-container {
  display: flex;
  justify-content: space-around;
}

.product-list,
.cart-content {
  width: 45%;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin-bottom: 10px;
}

button {
  margin-left: 10px;
}

p {
  font-weight: bold;
  margin-top: 20px;
}
</style>
