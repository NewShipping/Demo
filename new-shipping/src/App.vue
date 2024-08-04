<script setup>

import Header from './views/Header.vue'
import Aside from './views/Aside.vue'
import Main from './views/Main.vue'
</script>

<template>
  <el-container style="height: 100vh;">
    <el-header class="header-container">
      <Header></Header>      
    </el-header>
    <el-container style="height: calc(100% - 60px);">
      <el-aside class="aside-container">
        <Aside></Aside>
      </el-aside>
      <el-main>
        <Main></Main>
      </el-main>
    </el-container>
  </el-container>
</template>

<style scoped>
.header-container{
  border-bottom: 1px solid #dcdfe6;
}

.aside-container{
  border-right: 1px solid #dcdfe6;
}
</style>
