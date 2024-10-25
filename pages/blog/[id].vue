<template>
    <main>
        <h1>{{ route.params.id }}</h1>
    </main>
</template>
<script setup>
    const route = useRoute();
</script>