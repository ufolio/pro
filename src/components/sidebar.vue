<template>
    <ul>
        <sidebar-item
            v-for="item of items"
            :key="item.id"
            :item="item"
            :class="{ active: activeItem === item.id }"
            @click="activeItem = item.id"
        ></sidebar-item>
    </ul>
</template>

<script setup>
import { ref } from 'vue'
import sidebarItem from './SidebarItem.vue'

const items = [
    {
        id: 1, 
        name: 'Muzfon',
        domain: 'muzfon.pro',
        note: '',
    }, {
        id: 2, 
        name: 'PMK Group',
        domain: 'pmkgroup.ru',
        note: '',
    }, {
        id: 3, 
        name: 'Organic Spa',
        domain: 'spa-organic.ru',
        note: '',
    }
];

const activeItem = ref(1);

</script>