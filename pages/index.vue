<template>
  <div>
    <div>
      <p>page/index.vue</p>
      <TestButton />
    </div>
    <NuxtLink to="/hi/1" decoration-none>
      <button m-3 text-sm btn>
        GO
      </button>
    </NuxtLink>
    <n-card title="Home title">
      home
    </n-card>
  </div>
</template>
