<template>
    <main v-if="post">
        <h1>{{ post.title }}</h1>
        <div>
            {{ post.body }}
        </div>
    </main>
    <main v-else>
        <p>Chargement...</p>
    </main>
</template>
<script setup>
    const route = useRoute();
    const { data:post} = await useFetch('https://jsonplaceholder.typicode.com/posts/' + route.params.id,{
        lazy:true
    })
    useSeoMeta({
      title: ()=> post.value?.title
    })
</script>