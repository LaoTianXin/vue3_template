<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script lang="tsx" setup>
defineRender(() => {
  return <div>about</div>
})
</script>

<route lang="yaml">
meta:
  layout: default
</route>
