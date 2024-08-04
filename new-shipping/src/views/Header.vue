<script setup>   
</script>

<template>     
    <div class="header-wrapper">
        <p class="title">Logo</p>
        
        <div class="header-menu">
            <el-link>Shipping Agency</el-link>
        </div>
        
        <el-link :underline="false" class="user">
          <el-icon size="large"><UserFilled /></el-icon>
        </el-link>
    </div>    
</template>

<style scoped>
.header-wrapper{
  display: flex;
  flex-wrap: nowrap;
  flex-direction: row;
  justify-content: space-between;
  height: 100%;
  width: 100%;
}
.title{
  font-family: "Audiowide", sans-serif;  
  color: #409EFF;
  text-align: center;
}
.header-menu{
  display: flex;
  flex-wrap: nowrap;
  flex-direction: row;
  justify-content: space-around;
  font-family: "Audiowide", sans-serif;
}
.user{
  padding: 10px;
}
</style>