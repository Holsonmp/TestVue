<template>
    <h1>Your guide to everywhere</h1>
    <div class="">
        <article v-for="post in posts" :key="post.id">
            <h2>{{ post.title }}</h2>
            <div>
                <p>{{ post.body.slice(0, 100) }}</p>
            </div>
            <div>
                <NuxtLink :to="`/blog/${ post.id }`"> Lire la suite</NuxtLink>
            </div>

        </article>
    </div>

</template>
<script setup>
    const { data:posts, pending, error, refresh } = await useFetch('https://jsonplaceholder.typicode.com/posts?_limit=50',{
        
    })
</script>