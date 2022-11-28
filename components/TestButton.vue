<script setup lang="ts">
import { useDialog, useMessage, useNotification } from 'naive-ui'

const message = useMessage()
const dialog = useDialog()
const notification = useNotification()

function btnClick() {
  dialog.success({
    title: '成功',
    content: '厉害',
    positiveText: '哇',
    onPositiveClick: () => {
      message.success('我是message')
      notification.warning({
        content: '我是notification',
        duration: 3000,
      })
    },
  })
}
</script>

<template>
  <div m-2 flex justify-center gap-2>
    <n-button strong secondary type="info" @click="btnClick">
      strong secondary Info
    </n-button>
    <n-button strong secondary type="success" @click="btnClick">
      strong secondary Success
    </n-button>
    <n-button type="warning" @click="btnClick">
      Warning
    </n-button>
    <n-button type="error" @click="btnClick">
      Error
    </n-button>
  </div>
</template>
