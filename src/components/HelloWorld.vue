<script setup lang="ts">
defineEmits<{
  upadate: [id: number]
}>()

const count = defineModel<number>('count', { default: 0 })

const handleAddCount = () => {
  count.value++
}
</script>

<template>
  <div class="greetings">Hello, World!</div>
  <button @click="handleAddCount">ADD</button>
</template>

<style scoped></style>
