<script setup>
import Card from '../slots/card.vue';

const props = defineProps({
    ship: {
      type: Object,
      required: true
    },
    selectShip: {
      type: Function,
      required: true
    }
})

</script>

<template>
  <Card :click="props.selectShip">
    <template #edit>
      <el-icon><Edit /></el-icon>
    </template>
    {{ props.ship.name }}
    <template #delete>
      <el-icon><Delete /></el-icon>
    </template>    
  </Card>
</template>

<style scoped>
  
</style>
