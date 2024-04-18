<script setup lang="ts">

interface CardMainProps{
    id: number;
    title: string;
    body: string
}

const { id, title, body} = defineProps<CardMainProps>()
</script>

<template>
    <!-- <h2>Card</h2> -->

    <h2>{{ id }} - {{ title }}</h2>
    <p>{{ body }}</p>

    <NuxtLink :to="`/posts/${id}`">Leer mas</NuxtLink>
</template>