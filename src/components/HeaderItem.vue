<script setup lang="ts">
import type { FunctionalComponent, HTMLAttributes, VNodeProps } from 'vue';


const props = defineProps<{
    name: String,
    Icon: FunctionalComponent<HTMLAttributes & VNodeProps, {}, any>,
}>();

</script>

<template>
    <li class="flex flex-col items-center cursor-pointer w-20 sm:w-20 hover:text-white group">
        <Icon class="h-6 mb-1 group-hover:animate-bounce "/>
        <a class="uppercase opacity-0 group-hover:opacity-100 transition-all" href="#">{{ name }}</a>
    </li>
</template>