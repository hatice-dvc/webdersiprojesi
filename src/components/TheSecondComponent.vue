<template>
  <div class="login-container">
    <div class="login-box">
      <div class="greeting">
        <p class="greeting-title">Merhaba!</p>
        <p>Üyelere özel kupon ve fırsatlar seni bekliyor 🤗</p>
        <div class="card-header_tabs">
          <button
            class="login-button card-header__tabs-active"
            @click="goToLogin"
          >
            <span>Giriş Yap</span>
          </button>
          <button
            class="login-button card-header__tabs-active"
            @click="goToSignUp"
          >
            <span>Üye Ol</span>
          </button>
        </div>
      </div>
      <div class="login-form">
        <q-input v-model="email" label="E-posta Adresi" outlined />
        <q-input
          v-model="password"
          label="Şifre"
          type="password"
          outlined
          :append="{
            icon: passwordVisible ? 'visibility' : 'visibility_off',
            click: togglePasswordVisibility,
          }"
        />
      </div>
      <div class="full-width-mor-background" @click="handleButtonClick">
        <p class="full-width-text">Giriş Yap</p>
      </div>
      <div class="additional-options">
        <p class="before-after-style">
          ------------------------------- Diğer Seçenekler
          ----------------------------
        </p>
        <!-- Buraya istediğiniz ekstra seçenekleri ekleyebilirsiniz -->
      </div>
      <div class="social-buttons">
        <!-- Sosyal medya ile bağlanma butonları -->
        <button class="social-button" @click="loginWithGoogle">
          <img src="../assets/indir.png" style="width: 30px; height: 30px" />
        </button>

        <button class="social-button" @click="loginWithFacebook">
          <img src="../assets/indir2.png" style="width: 30px; height: 30px" />
        </button>

        <button class="social-button" @click="loginWithApple">
          <img src="../assets/indir3.png" style="width: 30px; height: 30px" />
        </button>
      </div>
      <div class="custom-button-container">
        <button class="custom-button">
          Yardıma mı ihtiyacın var? <br>
          0850 333 0011 numarası üzerinden Müşteri Hizmetleri'ni arayabilirsin.
        </button>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  data() {
    return {
      email: '',
      password: '',
      passwordVisible: false,
    };
  },
  methods: {
    login() {
      // Giriş işlemleri burada gerçekleştirilebilir
      console.log('E-posta:', this.email);
      console.log('Şifre:', this.password);
    },
    handleButtonClick() {
      // Burada tıklanabilir butonun işlemlerini gerçekleştirin
      this.login(); // veya başka bir metodunuzu çağırabilirsiniz
    },
    togglePasswordVisibility() {
      this.passwordVisible = !this.passwordVisible;
    },
    goToLogin() {
      // Giriş sayfasına yönlendirme işlemleri burada gerçekleştirilebilir
      console.log('Giriş Yap butonuna tıklandı');
    },
    goToSignUp() {
      // Üye ol sayfasına yönlendirme işlemleri burada gerçekleştirilebilir
      console.log('Üye Ol butonuna tıklandı');
    },
    loginWithGoogle() {
      console.log('Google ile giriş yap');
    },
    loginWithFacebook() {
      console.log('Facebook ile giriş yap');
    },
    loginWithApple() {
      console.log('Apple ile giriş yap');
    },
  },
});
</script>

<style scoped>
.login-container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

.login-box {
  max-width: 400px;
  width: 100%;
  padding: 20px;
  background-color: #fff; /* Arkaplan rengi beyaz */
  border: 1px solid #ccc;
  border-radius: 8px;
}

.greeting {
  text-align: center;
  margin-bottom: 20px;
}

.greeting-title {
  font-size: 24px; /* Örnek büyüklük, ihtiyaca göre ayarlayabilirsiniz */
  font-weight: bold;
  color: #333; /* Koyu renk, ihtiyaca göre ayarlayabilirsiniz */
}

.card-header_tabs {
  display: flex;
  justify-content: space-between; /* Butonları genişliğe göre dağıt */
  text-align: center;
}

.login-button {
  flex: 1; /* Butonları eşit genişlikte yap */
  max-width: 200px;
  width: 100%;
  padding: 10px;
  background-color: #fff; /* Arkaplan rengi beyaz */
  border: 1px solid #ccc;
  border-radius: 5px;
}

.login-button:hover {
  background-color: #ebf0f6; /* Renk ayarını ihtiyaca göre değiştirin */
}

.full-width-button {
  width: 100%;
}

.full-width-mor-background {
  background-color: rgb(90, 80, 166);
  color: white;
  text-align: center;
  padding: 10px;
  border-radius: 5px;
  margin-top: 20px;
}

.full-width-text {
  margin: 0;
}

.login-form q-input {
  position: relative;
  margin-bottom: 10px;
}

.login-form q-input i {
  position: absolute;
  right: 8px;
  top: 50%;
  transform: translateY(-50%);
  cursor: pointer;
}
.additional-options {
  margin-top: 20px;
}
.before-after-style {
  color: #6d6d6d; /* Rengi istediğiniz renkle değiştirin */
}
.before-after-style::before,
.before-after-style::after {
  content: '';
  display: inline-block;
  width: 10px; /* İstediğiniz genişliği ayarlayabilirsiniz */
}

.social-buttons {
  display: flex;
  justify-content: space-around;
  margin-top: 20px;
}
.social-button + .social-button {
  margin-left: 10px; /* İstediğiniz boşluğu ayarlayabilirsiniz */
}

.social-button {
  height: 50px;
  width: 100px;
  background-color: #ffffff; /* Google renk örneği */
  color: #766262;
  border: 1px solid #a7a7a7;
  border-radius: 5px;
  cursor: pointer;
}

.social-button:hover {
  background-color: #ffffff; /* Hover rengi */
}

.custom-button-container {
  margin-top: 20px; /* İstediğiniz boşluğu ayarlayabilirsiniz */
  width: 100%;
  text-align: center;
}

.custom-button {
  height: 100px;
  width: 100%;
  background-color: #f7fbf7; /* Örnek bir renk */
  color: #3a3939; /* Beyaz renk */
  padding-bottom: 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.custom-button:hover {
  background-color: #e2ede2; /* Hover rengi */
}
</style>
