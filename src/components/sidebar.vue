<template>
    <ul>
        <sidebar-item
            v-for="item of items"
            :key="item.id"
            :item="item"
            :class="{ active: activeItem === item.id }"
            @click="changeItem(item.id)"
        ></sidebar-item>
    </ul>
</template>

<script setup>
import { ref } from 'vue'
import sidebarItem from './SidebarItem.vue'

const items = [
    {id: 1, name: 'Muzfon'},
    {id: 2, name: 'PMK Group'},
    {id: 3, name: 'Organic Spa'},
];

var activeItem = ref(0);

function changeItem(id) {
    console.log(id);
    activeItem = id;
}

</script>