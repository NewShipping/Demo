<script setup>
    import voyage from "./voyage.vue";
    import cardAdd from "../slots/card-add.vue";

    const props = defineProps({
        selectVoyage: {
            type: Function,
            required: true
        },
        voyages: {
            type: Array,
            required: true
        }
    })

    function selectVoyage(){
        console.log('select a voyage');
    }
</script>

<template>
    <template v-for="(v, index) in voyages">
        <voyage :voyage="v" :select-voyage="selectVoyage"></voyage>
    </template>
    <card-add>
        <el-icon :size="'large'"><CirclePlus /></el-icon>
    </card-add>
</template>

<style scoped>
</style>