<script setup lang="ts">
import HeaderItem from '@/components/HeaderItem.vue';
import { HomeIcon, BoltIcon, CheckBadgeIcon, RectangleStackIcon, MagnifyingGlassIcon, UserIcon } from '@heroicons/vue/24/outline';


const links = [
    { name: "home", icon: HomeIcon },
    { name: "trending", icon: BoltIcon },
    { name: "verified", icon: CheckBadgeIcon },
    { name: "collections", icon: RectangleStackIcon },
    { name: "search", icon: MagnifyingGlassIcon },
    { name: "Account", icon: UserIcon },
];
</script>

<template>
    <header class="flex flex-col sm:flex-row m-5 justify-between items-center">
        <ul class="flex flex-grow justify-evenly max-w-2xl">
            <HeaderItem v-for="link of links" :key="link.name" :name="link.name" :Icon="link.icon"/>
        </ul>
        <img src="../assets/logo.webp" alt="hulu">
    </header>
</template>