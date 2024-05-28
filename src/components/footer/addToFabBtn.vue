<script setup lang="ts">
import {IonButton, IonIcon, IonToast} from "@ionic/vue";
import {star, starOutline} from 'ionicons/icons';
import {ref} from "vue";

const favorite = ref(false)
</script>

<template>
  <ion-button id="add-favorite-toast" class="favorite-btn  s-inactive" expand="block" v-show="!favorite"
              @click="favorite = true"></ion-button>
  <ion-toast trigger="add-favorite-toast"
             position="middle"
             :icon="star"
             message="This items added to your favorite list"
             :duration="5000"></ion-toast>

  <ion-icon id="remove-favorite-toast"
            slot="icon-only" class="favorite-btn" :icon="star" v-show="favorite" expand="block"
            style="cursor: pointer;"
            @click="favorite = false"></ion-icon>
  <ion-toast trigger="remove-favorite-toast"
             position="middle"
             :icon="starOutline"
             message="This items removed from your favorite list"
             :duration="5000"></ion-toast>

</template>

<style scoped>

</style>