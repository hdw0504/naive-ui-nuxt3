<template>
  <div>
    <div>
      <p>我在page/index.vue</p>
      <TestButton />
    </div>
    <NuxtLink to="/hi/1" decoration-none>
      <button m-3 text-sm btn>
        GO
      </button>
    </NuxtLink>
    <n-card title="首页">
      home
    </n-card>
  </div>
</template>
