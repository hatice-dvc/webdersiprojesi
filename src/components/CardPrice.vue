<template>
  <div class="q-pa-md">
    <!-- Sol üstteki görsel -->
    <div
      style="
        position: absolute;
        top: 0;
        left: 0;
        max-width: 100px;
        max-height: 100px;
      "
    >
      <q-img
        style="height: 100%; object-fit: contain"
        src="https://n11scdn.akamaized.net/a1/org/23/08/07/46/88/42/05/37/51/25/06/72/55884057542050464265.png"
      />
    </div>

    <!-- Quasar Carousel -->
    <q-carousel
      animated
      v-model="slide"
      arrows
      navigation
      infinite
      style="max-width: 220px; max-height: 225px"
    >
      <!-- Carousel Slides -->
      <q-carousel-slide :name="1">
        <q-img
          style="height: 100%; object-fit: contain"
          src="https://n11scdn.akamaized.net/a1/226_226/15/34/31/41/IMG-7706675353293360110.jpg"
          alt="Slide 1"
        />
      </q-carousel-slide>

      <q-carousel-slide :name="2">
        <q-img
          style="height: 100%; object-fit: contain"
          src="https://n11scdn.akamaized.net/a1/226_226/15/34/31/41/IMG-7706675353293360110.jpg"
          alt="Slide 2"
        />
      </q-carousel-slide>

      <q-carousel-slide :name="3">
        <q-img
          style="height: 100%; object-fit: contain"
          src="https://n11scdn.akamaized.net/a1/226_226/15/34/31/41/IMG-7706675353293360110.jpg"
          alt="Slide 3"
        />
      </q-carousel-slide>
    </q-carousel>

    <!-- Quasar Card -->
    <q-card class="my-card" flat bordered style="max-width: 300px">
      <!-- Card Header -->
      <q-card-section>
        <div class="row no-wrap items-center">
          <div class="col text-h6 ellipsis" style=" font-size: 15px; width: 300px;">
  The Mia Nutcracker Servis Tabağı 6'lı Set 26 Cm New 020</div>
          <div
            class="col-auto text-grey text-caption q-pt-md row no-wrap items-center"
          >
            <q-rating
              v-model="ratingModel"
              color="black"
              max="1"
              size="2em"
              icon="favorite_border"
              icon-selected="favorite"
              :color-selected="'purple-9'"
              style="cursor: pointer"
              @input="handleRatingChange"
            />
          </div>
        </div>

        <q-rating v-model="stars" :max="5" size="32px" />
      </q-card-section>

      <!-- Card Actions -->
      <q-card-actions>
        <q-btn flat round icon="event" />
        <q-btn flat color="primary"> Reserve </q-btn>
      </q-card-actions>
    </q-card>

    <!-- İncelediğin Ürünlere Benzer -->
    <h2 style="margin-top: 20px">İncelediğin Ürünlere Benzer 🤩</h2>
    <!-- Benzer ürünlerin listesi buraya eklenebilir -->
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const slide = ref<number>(1);
const stars = ref<number>(4);

const ratingModel = ref<number>(0);
const handleRatingChange = () => {
  // Rating değiştiğinde yapılacak işlemler
  console.log('Rating changed:', ratingModel.value);
};
</script>

<style scoped>
.my-card {
  border: 1px solid white;
  width: 100%;
}

/* q-img'nin boyutlarını istediğiniz gibi ayarlayabilirsiniz */
q-img {
  max-width: 100%;
  max-height: 150px;
}
</style>
