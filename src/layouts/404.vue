<template>
  <div>
    404
    <router-view />
    <div @click="router.go(-1)">back</div>
  </div>
</template>

<script setup lang="ts">
const router = useRouter()
</script>

<style scoped></style>
