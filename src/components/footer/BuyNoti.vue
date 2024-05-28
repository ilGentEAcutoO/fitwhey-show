<script setup lang="ts">
import {ref, onMounted} from 'vue'

const timer = ref(15);

onMounted(() => {
  const interval = setInterval(() => {
    timer.value--;
    if (timer.value === 0) {
      clearInterval(interval);
    }
  }, 1000);
});

</script>

<template>
  <div class="pd-noti-float" v-if="timer>0">
    <span class="noti-text">
      <img src="/assets/icon/mini-noti-icon.svg"> This product was last placed 2 minutes ago from Nonthaburi
    </span>
  </div>
</template>

<style scoped>

</style>