<script setup lang="ts">
const color = useColorMode()

function toggleDark() {
  color.preference = color.preference === 'dark' ? 'light' : 'dark'
}
</script>

<template>
  <p cursor-pointer m-x-auto class="dark:i-carbon-moon i-carbon-sun" @click="toggleDark" />
</template>
