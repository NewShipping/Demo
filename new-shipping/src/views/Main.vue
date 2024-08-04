<script setup>
import { Search } from '@element-plus/icons-vue'
import card from "../slots/card.vue"
import panel from "../slots/panel.vue"
import ships from "../components/ships.vue"
import voyagesComponent from "../components/voyages.vue"
import billsComponent from "../components/bills.vue"

const data = [
    { 
        name: "ship A",
        voyages: [
            {
                name: "voyage A in ship A",
                bills: [
                    {
                        id: "ABC123",
                        name: "steel",
                        weight: "100",
                        volume: "10",
                        shipper: "shipper A",
                        receiver: "receiver A",
                        comment: "something here"
                    }
                ]
            }
        ]
    },
    { 
        name: "ship A",
        voyages: [
            {
                name: "voyage A in ship A",
                bills: [
                    {
                        id: "ABC123",
                        name: "steel",
                        weight: "100",
                        volume: "10",
                        shipper: "shipper A",
                        receiver: "receiver A",
                        comment: "something here"
                    }
                ]
            }
        ]
    },
    { 
        name: "ship A",
        voyages: [
            {
                name: "voyage A in ship A",
                bills: [
                    {
                        id: "ABC123",
                        name: "steel",
                        weight: "100",
                        volume: "10",
                        shipper: "shipper A",
                        receiver: "receiver A",
                        comment: "something here"
                    }
                ]
            }
        ]
    },
    { 
        name: "ship A",
        voyages: [
            {
                name: "voyage A in ship A",
                bills: [
                    {
                        id: "ABC123",
                        name: "steel",
                        weight: "100",
                        volume: "10",
                        shipper: "shipper A",
                        receiver: "receiver A",
                        comment: "something here"
                    }
                ]
            }
        ]
    },
    { 
        name: "ship A",
        voyages: [
            {
                name: "voyage A in ship A",
                bills: [
                    {
                        id: "ABC123",
                        name: "steel",
                        weight: "100",
                        volume: "10",
                        shipper: "shipper A",
                        receiver: "receiver A",
                        comment: "something here"
                    }
                ]
            }
        ]
    },
    { 
        name: "ship A",
        voyages: [
            {
                name: "voyage A in ship A",
                bills: [
                    {
                        id: "ABC123",
                        name: "steel",
                        weight: "100",
                        volume: "10",
                        shipper: "shipper A",
                        receiver: "receiver A",
                        comment: "something here"
                    }
                ]
            }
        ]
    },
    { 
        name: "ship A",
        voyages: [
            {
                name: "voyage A in ship A",
                bills: [
                    {
                        id: "ABC123",
                        name: "steel",
                        weight: "100",
                        volume: "10",
                        shipper: "shipper A",
                        receiver: "receiver A",
                        comment: "something here"
                    }
                ]
            }
        ]
    },
    { 
        name: "ship A",
        voyages: [
            {
                name: "voyage A in ship A",
                bills: [
                    {
                        id: "ABC123",
                        name: "steel",
                        weight: "100",
                        volume: "10",
                        shipper: "shipper A",
                        receiver: "receiver A",
                        comment: "something here"
                    }
                ]
            }
        ]
    }
]

const voyages = [
    {
        name: "voyage A in ship A",
        bills: [
            {
                id: "ABC123",
                name: "steel",
                weight: "100",
                volume: "10",
                shipper: "shipper A",
                receiver: "receiver A",
                comment: "something qwertyuiopasdfghjklzxcvbnm"
            }
        ]
    },
    {
        name: "voyage A in ship A",
        bills: [
            {
                id: "ABC123",
                name: "steel",
                weight: "100",
                volume: "10",
                shipper: "shipper A",
                receiver: "receiver A",
                comment: "something here"
            }
        ]
    },
    {
        name: "voyage A in ship A",
        bills: [
            {
                id: "ABC123",
                name: "steel",
                weight: "100",
                volume: "10",
                shipper: "shipper A",
                receiver: "receiver A",
                comment: "something here"
            }
        ]
    },
    {
        name: "voyage A in ship A",
        bills: [
            {
                id: "ABC123",
                name: "steel",
                weight: "100",
                volume: "10",
                shipper: "shipper A",
                receiver: "receiver A",
                comment: "something here"
            }
        ]
    },
]

const bills = [
    {
        id: "ABC123",
        name: "steel",
        weight: "100",
        volume: "10",
        shipper: "shipper A",
        receiver: "receiver A",
        comment: "something qwertyuiopasdfghjklzxcvbnm"
    },
    {
        id: "ABC123",
        name: "steel",
        weight: "100",
        volume: "10",
        shipper: "shipper A",
        receiver: "receiver A",
        comment: "something here"
    }, 
    {
        id: "ABC123",
        name: "steel",
        weight: "100",
        volume: "10",
        shipper: "shipper A",
        receiver: "receiver A",
        comment: "something here"
    }, 
    {
        id: "ABC123",
        name: "steel",
        weight: "100",
        volume: "10",
        shipper: "shipper A",
        receiver: "receiver A",
        comment: "something here"
    }  
]

function selectShip(){
    console.log('select a ship')
}

function selectVoyage(){
    console.log('select a voyage')
}
</script>

<template>
    <el-row :gutter="20">
        <el-col :span="24">
        <div class="mt-4" style="font-family: Gill Sans, sans-serif; text-align: center;">
            <el-input v-model="input3" style="width: 600px" placeholder="Please input search content" class="input-with-select">
            <template #prepend>
                <el-select v-model="select" placeholder="Select" style="width: 115px">
                <el-option label="Ship Name" value="1" />
                <el-option label="Voyage No." value="2" />
                <el-option label="Bill No." value="3" />
                </el-select>
            </template>
            <template #append>
                <el-button :icon="Search" />
            </template>
            </el-input>
        </div>
        </el-col>
    </el-row>
    <br>
    <el-row :gutter="20" style="width: 100%; height: calc(100% - 60px);">
        <el-col :span="6" style="height: 100%">
            <panel>
                <ships :ships="data" :select-ship="selectShip"></ships>
            </panel>
        </el-col>
        <el-col :span="6" style="height: 100%">
            <panel>
                <voyages-component :voyages="voyages" :select-voyage="selectVoyage"></voyages-component>
            </panel>
        </el-col>
        <el-col :span="12" style="height: 100%">
            <panel>
                <bills-component :bills="bills"></bills-component>
            </panel>
        </el-col>
    </el-row>
</template>

<style scoped>
.plus-icon{
    color: #A8ABB2;
    vertical-align: baseline;
}
</style>