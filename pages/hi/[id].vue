<script setup lang="ts">
const route = useRoute()
const name = route.params.id

definePageMeta({
  layout: 'home',
})
</script>

<template>
  <div>
    <NuxtLink
      class="btn m-3 text-sm"
      to="/"
    >
      Back
    </NuxtLink>
    <n-card title="子页">
      {{ name }}!
    </n-card>

    <div />
  </div>
</template>
