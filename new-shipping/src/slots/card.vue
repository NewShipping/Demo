<script setup>
    import { ref } from 'vue';

    const props = defineProps({
        click: {
            type: Function,
            required: false
        },
        edit: {
            type: Function,
            required: false
        },
        delete: {
            type: Function,
            required: false
        }
    })

    var isHover = ref(false)

    function onClick(){
        if(props.click) props.click()
    }

    function hover(){
        isHover.value = !isHover.value;
    }
</script>

<template>
    <div class="card" v-on:mouseenter="hover" v-on:mouseleave="hover">
        <div class="card-edit" v-if="isHover">
            <slot name="edit"></slot>
        </div>
        <div class="card-main" v-on:click="onClick">
            <slot></slot>
        </div>
        <div class="card-delete" v-if="isHover">
            <slot name="delete"></slot>
        </div>
    </div>
</template>

<style scoped>
.card{
    text-align: center;
    margin-left: 10px;
    margin-right: 10px;
    font-family: "Open Sans", sans-serif;
    border-width: 0.1em;
    border-style: solid;
    border-color: #c6e2ff;
    border-radius: 10px;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-content: center;   
}

.card-main{
    padding-top: 10px;
    padding-bottom: 10px;
}

.card:hover{    
    background-color: #c6e2ff;
    color: white;
    justify-content: space-between;
    cursor: pointer;
}

.card:hover > .card-edit{
    background-color: #ebb563;
    color: #FFFFFF;
    padding:10px;
    margin-top: -0.1em;
    margin-bottom: -0.1em;
    margin-left: -0.1em;
    border-top-left-radius: 10px;
    border-bottom-left-radius: 10px;
    align-content: center; 
}

.card:hover > .card-delete{
    background-color: #f78989;
    color: #FFFFFF;
    padding:10px;
    margin-top: -0.1em;
    margin-bottom: -0.1em;
    margin-right: -0.1em;
    border-top-right-radius: 10px;
    border-bottom-right-radius: 10px;
    align-content: center; 
}
</style>