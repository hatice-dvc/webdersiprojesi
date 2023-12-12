<template>
  <div class="q-pa-md">
    <q-carousel
      animated
      v-model="slide"
      navigation
      infinite
      :autoplay="autoplay"
      arrows
      transition-prev="slide-right"
      transition-next="slide-left"
      @mouseenter="autoplay = false"
      @mouseleave="autoplay = true"
    >
    <q-carousel-slide
        :name="1"
        img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/08/67/78/58/61/33/73/94/78/77/94460984954828340413.jpg"
      >
      </q-carousel-slide>
      <q-carousel-slide
        :name="2"
        img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/09/71/24/67/12/57/57/63/39/74/23255475412697172254.jpg"
      >
        <div>
          <q-carousel-control
            position="top-right"
            :offset="[100, 100]"
            class="text-white rounded-borders"
            style="
              background: #f6f5f7;
              height: 180px;
              width: 350px;
              display: flex;
              align-items: flex-end;
            "
          >
            <div style="padding: 20px 20px 0 8px; color: #5a3d8c; font-weight: bold;">
              <p style="margin-top: 50px; font-size: 13px;">Sabah 09.00'a kadar geçerli!</p>
              <p style="font-size: 28px;">Gecenin sürprizini kaçırma!</p>
            </div>

            <q-btn color="purple" text-color="white" label="Ürüne Git " />/>
          </q-carousel-control>
        </div>
      </q-carousel-slide>
      <q-carousel-slide/>
      <q-carousel-slide :name="3" img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/09/64/64/58/98/75/21/37/55/68/64757561397295401386.jpg" />
      <q-carousel-slide :name="4" img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/08/58/03/49/80/37/91/66/45/89/23603055386349056343.jpg" />
      <q-carousel-slide :name="5" img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/08/79/92/99/07/10/82/28/28/89/51324589523414895162.jpg" />
      <q-carousel-slide :name="6" img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/09/51/22/16/31/83/04/61/22/76/77092101554917033911.jpg" />
      <q-carousel-slide :name="7" img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/08/64/05/24/33/29/81/16/64/91/12869060756402094097.jpg" />
      <q-carousel-slide :name="8" img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/08/59/12/52/88/33/41/08/33/75/2397229034675456405.jpg" />
      <q-carousel-slide :name="9" img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/08/54/53/04/38/74/18/12/36/61/43801001994166616542.jpg" />
      <q-carousel-slide :name="10" img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/08/91/87/83/68/99/97/37/24/07/9797683925718157762.png" />
      <q-carousel-slide :name="11" img-src="https://n11scdn.akamaized.net/a1/1180_440/23/12/08/88/34/56/49/13/35/95/03/35/0647674624997018734.jpg" />
    </q-carousel>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      slide: ref(1),
      autoplay: ref(true)
    }
  }
}
</script>
