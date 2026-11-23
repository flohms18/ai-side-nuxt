<script setup lang="ts">

import type { NavigationMenuItem } from '@nuxt/ui';

const route = useRoute()

const items = computed<NavigationMenuItem[]>(() => [
    {
        label : 'Docs',
        to : 'about',
        active : route.path.startsWith('/about')
    }
])


</script>




<template>
    <UHeader>
        <template #title >

        </template>

        <template #right>
            <UNavigationMenu :items="items" />
        </template>
    </UHeader>
    </template>