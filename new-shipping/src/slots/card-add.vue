<script setup>
    const props = defineProps({
        click: {
            type: Function,
            required: false
        }
    })

    function onClick(){
        if(props.click) props.click()
    }

</script>

<template>
    <div class="card-add" v-on:click="onClick">
        <slot></slot>
    </div>
</template>

<style scoped>
    .card-add{        
        margin-left: 10px;
        margin-right: 10px;
        font-family: "Open Sans", sans-serif;
        border-width: 0.1em;
        border-style: solid;
        border-color: transparent;
        border-radius: 10px;
        text-align: center;    
        align-content: center;
        padding-top: 10px;
        padding-bottom: 10px;
        color: #A8ABB2;
    }

    .card-add:hover{    
        background-color: #c6e2ff;
        color: white;
        cursor: pointer;
    }
</style>