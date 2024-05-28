<script setup lang="ts">
import {IonHeader, IonToolbar, IonButton, IonButtons, IonBadge} from "@ionic/vue";

const emit = defineEmits(['cart-modal'])
</script>

<template>
  <ion-header mode="md" class="top-header-wrap ion-no-border fixed">
    <ion-toolbar class="toolbar-wrap clear">
      <ion-buttons slot="start">
        <ion-button class="header-btn back-btn">
          <img src="/assets/icon/white-back-arrow-icon.svg" alt="" class="">
        </ion-button>
      </ion-buttons>
      <ion-buttons slot="primary" class="icon-btn">
        <ion-button @click="emit('cart-modal')">
          <ion-badge class="noti-count">2</ion-badge>
          <img src="/assets/icon/cart-icon.svg" alt="" class="icon-size">
        </ion-button>
        <ion-button>
          <ion-badge class="noti-count">99</ion-badge>
          <img src="/assets/icon/message-icon.svg" alt="" class="icon-size message">
        </ion-button>
      </ion-buttons>
    </ion-toolbar>
    <!-- order purchase noti -->
    <!--
    <div class="pd-noti-float">
        <span class="noti-text"><img src="/assets/icon/mini-noti-icon.svg"> This product was last placed 2 minutes ago from Nonthaburi</span>
    </div>
    -->
  </ion-header>
</template>

<style scoped>

</style>