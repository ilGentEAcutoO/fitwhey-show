<script setup lang="ts">
import {chevronBackCircleOutline} from "ionicons/icons";
import {ref} from "vue";
import {
  IonIcon,
  IonButtons,
  IonButton,
} from "@ionic/vue";
const sizeNow = ref(0)

</script>

<template>
  <ion-buttons class="pd-size-slider-tab">
    <ion-button class="size-sub-btn inactive">
      <ion-icon :icon="chevronBackCircleOutline"></ion-icon>
    </ion-button>
    <ion-button class="size-sub-btn " :class="[sizeNow == 0 ? 'active' : 'inactive']" @click="sizeNow = 0">Sample
    </ion-button>
    <ion-button class="size-sub-btn " :class="[sizeNow == 1 ? 'active' : 'inactive']" @click="sizeNow = 1">250g
    </ion-button>
    <ion-button class="size-sub-btn " :class="[sizeNow == 2 ? 'active' : 'inactive']" @click="sizeNow = 2">2lb
    </ion-button>
    <ion-button class="size-sub-btn " :class="[sizeNow == 3 ? 'active' : 'inactive']" @click="sizeNow = 3">5lb
    </ion-button>
    <ion-button class="size-sub-btn " :class="[sizeNow == 4 ? 'active' : 'inactive']" @click="sizeNow = 4">10lb
    </ion-button>
    <ion-button class="size-sub-btn " :class="[sizeNow == 5 ? 'active' : 'inactive']" @click="sizeNow = 5">12lb
    </ion-button>
  </ion-buttons>
</template>

<style scoped>

</style>