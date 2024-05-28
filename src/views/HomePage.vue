<template>
  <ion-page style="max-width: 1024px; margin: 0 auto;">
      <!-- header -->
      <fw-header @cart-modal="openCartModal" />
      <!-- mid content -->
      <fw-content />
      <!-- bottom fixed tab -->
      <fw-footer @cart-modal="openCartModal" v-if="!showCartModal"/>
      <!-- modal -->
      <ion-backdrop v-if="showCartModal" @click="closeModal"></ion-backdrop>
      <fw-cart-modal id="box" :show="showCartModal" @closeModal="closeModal"/>
  </ion-page>
</template>

<script setup lang="ts">
import {IonPage, IonBackdrop} from '@ionic/vue';
import {ref} from 'vue';
import FwHeader from "@/components/header/FwHeader.vue";
import FwFooter from "@/components/footer/FwFooter.vue";
import FwContent from "@/components/content/FwContent.vue";
import FwCartModal from "@/components/checkout/FwCartModal.vue";

const showCartModal = ref(false)

function openCartModal() {
  showCartModal.value = true
}

function closeModal() {
  showCartModal.value = false
}
</script>

<style scoped>
#container {
  text-align: center;

  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;

  color: #8c8c8c;

  margin: 0;
}

#container a {
  text-decoration: none;
}
ion-backdrop {
  background: var(--ion-color-dark);
  opacity: 0.3;
}

#box {
  position: absolute;
  top: 58%;
  left: 50%;
  transform: translateY(-50%) translateX(-50%);
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--ion-background-color, #fff);
  width: 90%;
  height: 100px;
  border-radius: 10px;
}
</style>
