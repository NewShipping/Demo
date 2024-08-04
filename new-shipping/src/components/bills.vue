<script setup>
    import bill from './bill.vue';
    import cardAdd from "../slots/card-add.vue"

    const props = defineProps({
        bills: {
            type: Array,
            required: true
        }
    })
</script>

<template>
    <template v-for="(b, i) in props.bills">
        <bill :bill="b"></bill>
    </template>
    <card-add>
        <el-icon :size="'large'"><CirclePlus /></el-icon>
    </card-add> 
</template>