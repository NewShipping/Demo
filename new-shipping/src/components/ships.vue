<script setup>   
    import ship from "./ship.vue";
    import cardAdd from "../slots/card-add.vue"

    const props = defineProps({
        selectShip: {
            type: Function,
            required: true
        },
        ships: {
            type: Array,
            required: true
        }
    })

    function selectShip(){
        console.log('select a ship');
    }
</script>

<template>
    <template v-for="(s, index) in ships">
        <ship :ship="s" :select-ship="selectShip"></ship>
    </template>
    <card-add>
        <el-icon :size="'large'"><CirclePlus /></el-icon>
    </card-add>  
</template>

<style scoped>

</style>