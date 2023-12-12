<template>
  <div>
    <div class="d-flex flex-row justify-content-center">
      <div class="row">
        <div class="col-md">
          <form>
            <div class="sign-in mb-3">Hesap Oluşturun</div>

            <div class="form-group mb-3" style="margin-top: 2vh">
              <div>
                <label for="exampleInputName" style="font-weight: bold"
                  >Ad - Soyad</label
                >
              </div>
              <div>
                <input
                  type="text"
                  class="form-control btn1"
                  id="exampleInputName"
                  placeholder="Adı ve soyadı"
                />
              </div>
            </div>

            <div class="form-group mb-3" style="margin-top: 2vh">
              <div>
                <label for="exampleInputEmail1" style="font-weight: bold"
                  >E-posta</label
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

            <div class="form-group mb-3" style="margin-top: 2vh">
              <div>
                <label for="exampleInputPassword1" style="font-weight: bold"
                  >Şifre</label
                >
              </div>
              <div>
                <input
                  type="password"
                  class="form-control btn1"
                  id="exampleInputPassword1"
                  placeholder="En az 6 karakter"
                />
              </div>
            </div>

            <div class="form-group mb-3" style="margin-top: 2vh">
              <div>
                <label for="exampleInputPassword2" style="font-weight: bold"
                  >Şifreyi tekrar girin</label
                >
              </div>
              <div>
                <input
                  type="password"
                  class="form-control btn1"
                  id="exampleInputPassword2"
                />
              </div>
            </div>
            <div class="form-group mb-3">
              <div class="form-check">
                <input
                  type="checkbox"
                  class="form-check-input"
                  id="exampleCheck1"
                />
                <label class="form-check-label" for="exampleCheck1">
                  Amazon’dan teklif ve promosyonlar da dahil olmak üzere ticari
                  elektronik ileti (e-posta ve SMS gibi) almayı ve Amazon’un
                  kişisel verilerimi aynı amaçla işlemesini kabul ediyorum.
                  *Yasalar gereği e-posta adresinizi İleti Yönetim Sistemi A.Ş.
                  (“İYS”) ile paylaşacağız. İYS’nin veri güvenliği konusunda
                  aldığı tedbirler üzerinde herhangi bir kontrolümüz
                  bulunmamaktadır.
                </label>
              </div>
            </div>

            <div class="form-group text-center mb-3">
              <button
                type="submit"
                class="btn bg-warning text-dark"
                id="signUp"
              >
                Amazon hesabınızı oluşturun
              </button>
              <p class="mb-3" style="margin-top: 2vh">
                Bir hesap oluşturduğunuzda, Amazon'un Kullanım ve Satış
                Koşulları'nı kabul etmiş olursunuz. Daha fazla bilgi için
                Gizlilik Bildirimi, Çerez Bildirimi ve İlgi Alanına Dayalı
                Tanıtımları inceleyebilirsiniz.
              </p>
              <a href="#">Yardımamı ihtiyacınız var?</a>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
@import '../static/style.css';
</style>
