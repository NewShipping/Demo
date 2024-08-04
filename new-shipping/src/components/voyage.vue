<script setup>
    import Card from "../slots/card.vue"    

    const props = defineProps({
        voyage: {
            type: Object,
            required: true
        },
        selectVoyage: {
            type: Function,
            required: true
        }
    })
</script>

<template>
    <Card :click="props.selectVoyage">
        <template #edit>
            <el-icon><Edit /></el-icon>
        </template>
        {{ props.voyage.name }}
        <template #delete>
            <el-icon><Delete /></el-icon>
        </template> 
    </Card>
</template>

<style scoped></style>