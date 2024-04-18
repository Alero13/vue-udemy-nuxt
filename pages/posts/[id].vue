<script setup lang="ts">
import type { Post } from '~/interfaces/posts.type';


/* const route = useRoute()  */
const {id} = useRoute().params

/* console.log(route.params.id) */

const { data: post}  = await useFetch<Post>(`https://jsonplaceholder.typicode.com/posts/${id}`)
</script>

<template>
    <h1>Post Page id: {{ id }}</h1>

    <!-- <CardMain
        :id="post?.id"
        :title="post?.title"
        :body="post?.body"
    /> -->

    <h2>{{ post?.title }}</h2>
    <p>{{ post?.body }}</p>
</template>