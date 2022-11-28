<script lang="ts" setup>
import { darkTheme, lightTheme } from 'naive-ui'

const color = useColorMode()
const theme = computed(() => color.preference === 'dark' ? darkTheme : lightTheme)

useHead({
  title: 'Vitesse Nuxt 3',
  link: [
    {
      rel: 'icon', type: 'image/png', href: '/nuxt.png',
    },
  ],
})

watch(() => color.preference, () => {
  console.log('color.preference', color.preference)
})
</script>

<template>
  <n-config-provider :theme="theme">
    <n-message-provider>
      <n-notification-provider>
        <n-loading-bar-provider>
          <n-dialog-provider>
            <!-- 在这里没问题 -->
            <div text-center>
              <p>app.vue</p>
              <TestButton />
            </div>
            <!-- 下面layout不对 -->
            <NuxtLayout>
              <NuxtPage />
            </NuxtLayout>
          </n-dialog-provider>
        </n-loading-bar-provider>
      </n-notification-provider>
    </n-message-provider>
  </n-config-provider>
</template>

<style>
*{
  margin: 0;
  padding: 0;
}
html, body , #__nuxt{
  height: 100vh;
  margin: 0;
  padding: 0;
}

html.dark {
  background: #222;
  color: white;
}
</style>
