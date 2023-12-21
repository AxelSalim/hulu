<script setup lang="ts">
import requests from "@/utils/request";

const genreList: string[] = [];

Object.entries(requests).forEach(([key, {title, url}]) => {
    genreList.push(title);
})

</script>

<template>
    <nav>
        <!-- <ul class="flex px-10 sm:px-20 text-2xl whitespace-nowrap gap-10 sm:gap-20 overflow-x-scroll">
            <li v-for="request of requests" :key="request">
                <button>{{ request.title }}</button>
            </li>
        </ul> -->

        <ul class="flex px-10 sm:px-20 text-2xl whitespace-nowrap gap-10 sm:gap-20 overflow-x-scroll scrollbar-hide">
            <li v-for="genre of genreList" :key="genre" class="transition duration-300 transform hover:scale-125 hover:text-white active:text-red-500">
                <button>{{ genre }}</button>
            </li>

        </ul>
    </nav>
</template>