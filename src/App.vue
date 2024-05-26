<script setup>
import { useUserStore } from '@/stores/modules/user'

const userStore = useUserStore()
</script>

<template>
  <RouterView></RouterView>

  <hr />
  <hr />
  <div>123</div>
  <p>{{ userStore.token }}</p>
  <el-button type="primary" @click="userStore.setToken('abcdefg')"
    >登录</el-button
  >
  <el-button type="danger" @click="userStore.removeToken()">退出</el-button>
</template>

<style scoped></style>
