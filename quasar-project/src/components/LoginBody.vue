<template>
  <q-page>
    <div class="d-flex flex-row justify-content-center">
      <div>
        <div>
          <q-form>
            <div class="sign-in">Giriş Yap</div>
            <div class="form-group mb-3">
              <div>
                <label for="exampleInputEmail1" style="font-weight: bold"
                  >E-posta adresi veya telefon numarası</label
                >
              </div>
              <div>
                <input
                  type="email"
                  class="form-control btn1"
                  id="exampleInputEmail1"
                  aria-describedby="emailHelp"
                />
              </div>
            </div>
            <div class="form-group">
              <div class="button-container">
                <routerLink to="/">
                  <q-btn class="btn bg-warning text-dark" no-caps
                    >Devam Et</q-btn
                  ></routerLink
                >
              </div>
              <q-parcel>
                <p style="margin-top: 2vh">
                  Oturum açarak, Amazon'un Kullanım ve Satış Koşulları'nı kabul
                  etmiş olursunuz. Kişisel verilerinizin Amazon tarafından nasıl
                  işlendiğine ilişkin detaylı bilgi için Gizlilik Bildirimi,
                  Çerez Bildirimi ve İlgi Alanına Dayalı Tanıtımları
                  inceleyebilirsiniz.
                </p>
              </q-parcel>
              <q-parcel
                ><p>
                  <q-link to="^#">Yardımamı ihtiyacınız var?</q-link>
                </p>
              </q-parcel>
            </div>

            <div class="form-check"></div>
            <router-link to="signup">
              <q-btn class="btn bg-white text-dark" no-caps>
                Amazon Hesabınızı Oluşturun!</q-btn
              >
            </router-link>
          </q-form>
        </div>
      </div>
    </div>
  </q-page>
</template>

<style>
@import '../static/style.css';
</style>
