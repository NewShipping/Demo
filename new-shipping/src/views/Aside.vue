<script setup>   
</script>

<template>            
    <div class="aside-menu">
        <p></p>
        <p style="text-align: center;">
          <el-link :underline="false">Main Dashboard</el-link>
        </p>
        <p style="text-align: center;">
          <el-link :underline="false">Shipper Company</el-link>
        </p>
        <p style="text-align: center;">
          <el-link :underline="false">Receiver Company</el-link>
        </p>
    </div>    
</template>

<style scoped>
.aside-menu{  
  width: 85%;
  display: flex;
  flex-wrap: nowrap;
  flex-direction: column;
  font-family: "Audiowide", sans-serif;
  margin-left: auto;
  margin-right: auto;
  margin-top: 8px;
  align-content: space-around;
  row-gap: 8px;
  border: unset;
}
.aside-menu .el-link{
  padding: 4px;
}
</style>