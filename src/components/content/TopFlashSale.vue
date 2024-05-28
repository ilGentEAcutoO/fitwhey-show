<script setup lang="ts">
import { ref, onMounted } from 'vue'

const hours = ref(0)
const minutes = ref(12)
const seconds = ref(24)

onMounted(() => {
  const interval = setInterval(() => {
    seconds.value--
    if (seconds.value < 0) {
      seconds.value = 59
      minutes.value--
      if (minutes.value <= 0) {
        seconds.value = 0
        minutes.value = 0
        clearInterval(interval)
        return
      }
    }
  }, 1000)

})

</script>

<template>
  <div class="pd-flash-wrap">
    <span class="flash-header">Flash Sale</span>
    <span class="timer">
                        <ul>
                            <li>{{ hours }}</li> :
                            <li>{{ minutes }}</li> :
                            <li>{{ seconds }}</li>
                        </ul>
                    </span>
  </div>

</template>

<style scoped>

</style>