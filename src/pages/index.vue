<script setup lang="ts">
import { registerSW } from 'virtual:pwa-register'
const count = ref(0)

const time = 30 * 60 * 60 * 1000
onMounted(() => {
  registerSW({
    immediate: true,
    onRegisteredSW(_url, registration) {
      registration &&
        setInterval(() => {
          registration.update()
        }, time)
    }
  })
})
</script>

<template>
  <main>
    <icon-mdi-account />
    <div>{{ count }}</div>
    <HelloWorld v-model:count="count" />
    <ReloadPrompt></ReloadPrompt>
  </main>
</template>
