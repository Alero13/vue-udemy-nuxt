<script setup lang="ts">

import type { Post } from "@/interfaces/posts.type"

    /* const {data: posts } = await useFetch("https://jsonplaceholder.typicode.com/posts") */

    const {data: posts } = await useFetch<Post[]>("https://jsonplaceholder.typicode.com/posts")

    /* console.log(data.value) */
</script>

<template>
    <h1>Posts Page </h1>

    <!-- <pre>{{ posts[0].title }}</pre> -->

    <!-- <pre>{{ posts[0].id }}</pre> -->

    <!-- <pre>{{ posts }}</pre> -->

    <!-- <CardMain 
        v-for="post in posts"
        :key="post.id"
        :title="post.title"
        :body="post.body"
    /> -->

    <CardMain 
        v-for="{id, title, body } of posts"
        :key="id"
        :title="title"
        :body="body"
        :id="id"
    />
</template>