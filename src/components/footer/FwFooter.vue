<script setup lang="ts">
import {IonToolbar, IonFooter, IonButtons, IonButton} from "@ionic/vue";
import  {defineEmits} from "vue";
import BuyNoti from "@/components/footer/BuyNoti.vue";
import AddToFabBtn from "@/components/footer/addToFabBtn.vue";

const emit = defineEmits(['cart-modal'])
</script>

<template>
  <ion-footer class="footer-menu-common">
    <buy-noti/>
    <ion-toolbar class="menu-bar-wrap">
      <ion-buttons class="menu-btn">
        <add-to-fab-btn />
        <ion-button class="main-footer-btn active" @click="emit('cart-modal')">Add to Cart</ion-button>
      </ion-buttons>
    </ion-toolbar>
  </ion-footer>
</template>

<style scoped>

</style>