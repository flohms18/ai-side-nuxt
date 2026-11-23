<script setup lang="ts">

import type { NavigationMenuItem } from '@nuxt/ui'


const route = useRoute()

const items = computed<NavigationMenuItem[]>(() => [
    {
        label : 'About',
        to : 'about',
        active : route.path.startsWith('/about')
    }
])

</script>


<template>
    <UFooter>
        <template #left>
            Hello There
        </template>

        <UNavigationMenu :items="items" variant="link" />

        <template #right>
            James Bond
        </template>
    </UFooter>
    </template>