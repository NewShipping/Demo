<script setup></script>

<template>
    <div class="col-panel-wrapper">
        <div class="col-panel">
            <slot></slot>
        </div>
    </div>
</template>

<style scoped>
    .col-panel-wrapper{
        width: 100%;
        height: 100%;
        padding-top: 10px;
        padding-bottom: 10px;
        border: 1px solid #c6e2ff;
        border-radius: 10px;
        box-shadow: 0px 0px 6px rgba(0, 0, 0, .12);
    }

    .col-panel{
        width: 100%;
        height: 100%;
        overflow-y: auto;
        display: flex;
        flex-direction: column;
        row-gap: 10px;
    }

    .col-panel:hover::-webkit-scrollbar-thumb {
        background: #c6e2ff;
    }

    /* width */
    .col-panel::-webkit-scrollbar {
        width: 3px;
    }

    /* Track */
    .col-panel::-webkit-scrollbar-track {
        background: transparent;
        border-radius: 3px;
    }
    
    /* Handle */
    .col-panel::-webkit-scrollbar-thumb {
        background: transparent;
        border-radius: 3px;
    }
</style>