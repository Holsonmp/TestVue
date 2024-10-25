<template>
    <main>
        <h1>{{ post.title }}</h1>
        <div>
            
        </div>
    </main>
</template>
<script setup>
    const route = useRoute();
    const { data:post, pending, error, refresh } = await useFetch('https://jsonplaceholder.typicode.com/posts/' + route.params.id,{
        
    })
</script>