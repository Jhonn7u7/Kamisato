<template>
    <h2 :id="id" class="font-extrabold text-2xl md:text-3xl m-0 text-indigo-900">
        <slot />
    </h2>
</template>

<script setup lang="ts">
defineProps<{ id: string }>()
</script>
