<template>
    <div>
        <h1>{{ data.hello }}</h1>
    </div>
</template>
<script setup>
    const { data, pending, error, refresh } = await useFetch('/api/hello',{
        
    })
</script>