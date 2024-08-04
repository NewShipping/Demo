<script setup>    
    import {computed, ref} from 'vue';
    import Card from '../slots/card.vue';

    const props = defineProps({
        bill: {
            type: Object,
            required: true
        }
    })
</script>

<template>
    <Card>
        <template #edit>
            <el-icon><Edit /></el-icon>
        </template>
        <el-descriptions :column="3" :size="'small'" :border="true">
            <el-descriptions-item>
                <template #label>bill no.</template>
                {{ props.bill.id }}
            </el-descriptions-item>
            <el-descriptions-item>
                <template #label>weight</template>
                {{ props.bill.weight }}
            </el-descriptions-item>
            <el-descriptions-item>
                <template #label>volume</template>
                {{ props.bill.volume }}
            </el-descriptions-item>
            <el-descriptions-item :span="1.5">
                <template #label>shipper</template>
                {{ props.bill.shipper }}
            </el-descriptions-item>
            <el-descriptions-item :span="1.5">
                <template #label>receiver</template>
                {{ props.bill.receiver }}
            </el-descriptions-item>
            <el-descriptions-item :span="3">
                <template #label>comment</template>
                {{ props.bill.comment }}
            </el-descriptions-item>
        </el-descriptions>
        <template #delete>
            <el-icon><Delete /></el-icon>
        </template>
    </Card>
</template>

<style scoped>
    
</style>