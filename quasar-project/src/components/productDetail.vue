<template>
  <q-page>
    <q-container>
      <q-row class="justify-center">
        <q-col cols="12" md="6">
          <q-card>
            <q-card-section>
              <div
                class="preview-pic tab-content"
                style="height: auto; width: auto"
              >
                <img
                  src="src\static\p1.jpg"
                  alt="Product Preview"
                  style="max-height: auto; width: 200px"
                /></div
            ></q-card-section>

            <q-card-section>
              <q-row>
                <q-col cols="12" md="6">
                  <div class="details">
                    <h3 class="product-title">Kulaklık</h3>
                    <div class="rating">
                      <div class="stars">
                        <span class="fa fa-star checked"></span>
                        <span class="fa fa-star checked"></span>
                        <span class="fa fa-star checked"></span>
                        <span class="fa fa-star"></span>
                        <span class="fa fa-star"></span>
                      </div>
                      <span class="review-no">100 görüntülenme</span>
                    </div>
                    <p class="product-description">
                      Bu ürün hakkında: Kablolu kulaklık Menşe Ülke: Amerika
                      Birleşik Devletleri 7.1 Sanal Surround Ses Dijital ses
                      iyileştirme özellikli mikrofon 53 mm'lik sürücülerle HiFi
                      özellikli, gürültü azaltma, AGC işlevi ve yankı azaltma
                      özellikleri
                    </p>
                    <h4 class="price">Fiyat <span>800 TL</span></h4>
                    <p class="vote">
                      <strong>91%</strong> of buyers enjoyed this product!
                      <strong>(87 votes)</strong>
                    </p>

                    <h5 class="colors">
                      Colors:
                      <span class="color green"></span>
                      <span class="color blue"></span>
                    </h5>
                    <div class="action">
                      <q-btn
                        color="primary"
                        @click="addToCart"
                        label="Sepete Ekle"
                      />
                    </div>
                  </div>
                </q-col>
              </q-row>
            </q-card-section>
          </q-card>
        </q-col>
      </q-row>
    </q-container>
  </q-page>
</template>

<script setup>
function addToCart() {
  // Sepete ekleme işlemleri burada gerçekleştirilebilir.
  alert('Ürün sepete eklendi');
}
</script>

<style>
@import '../static/style.css';
.q-card {
  display: flex;
}
</style>
