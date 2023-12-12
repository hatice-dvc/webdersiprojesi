<template>
  <q-list>
    <q-item class="column" style="width: 100%; display: inline-block">
      <q-card>
        <q-link
          to="https://www.n11.com/urun/bimotif-dokuma-ekoseden-15-parca-4-kisilik-yilbasi-sofra-seti-1-44764673?magaza=bimotif"
          class="plink"
          data-id="588585302"
          title="Bimotif Dokuma Ekoseden 15 Parça, 4 Kişilik Yılbaşı Sofra Seti 1"
          tabindex="0"
        >
          <q-img
            class="lazy cardImage"
            :src="imageSrc"
            :alt="productName"
            style="opacity: 1"
          />
          <q-badge
            color="primary"
            title="Favorilere ekle"
            :data-productid="productId"
          ></q-badge>
          <div class="heartIcon" @click="toggleFavorite">
            <q-icon
              :name="isFavorite ? 'favorite' : 'favorite_border'"
              class="cursor-pointer"
            />
          </div>
          <q-badge color="positive" class="cargoBadgeField">
            <span class="cargoBadgeText">ÜCRETSİZ KARGO</span>
          </q-badge>
          <q-card-section>
            <q-item-label class="text-h6 productName">{{
              productName
            }}</q-item-label>
          </q-card-section>
        </q-link>
        <q-card-section>
          <div class="priceContainer">
            <div>
              <q-item-label
                class="oldPrice noLine cPoint priceEventClick"
                :title="productName"
              >
                649 TL
              </q-item-label>
              <q-badge color="primary" class="specialPriceTitle colorR60">
                SEPETTE
              </q-badge>
              <q-item-label
                class="newPrice cPoint priceEventClick"
                :title="productName"
              >
                <ins>551,65 TL</ins>
              </q-item-label>
            </div>
          </div>
        </q-card-section>
      </q-card>
    </q-item>
  </q-list>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const imageSrc = ref(
  'https://n11scdn.akamaized.net/a1/226_226/11/53/96/47/IMG-8518729972870146433.jpg'
);
const productName = ref(
  'Bimotif Dokuma Ekoseden 15 Parça, 4 Kişilik Yılbaşı Sofra Seti 1'
);
const productId = ref('588585302');
const isFavorite = ref(false);

const toggleFavorite = () => {
  isFavorite.value = !isFavorite.value;
};
</script>

<style scoped>
.column {
  max-width: 300px;
  margin: 0 auto;
}

.cardImage {
  max-width: 100%;
  height: auto;
}

.productName {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.priceContainer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.oldPrice,
.newPrice {
  margin-right: 5px;
}

.heartIcon {
  position: absolute;
  top: 10px;
  right: 10px;
  cursor: pointer;
}
</style>
