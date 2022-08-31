<template>
    <h3 :id="id" class="font-extrabold text-xl md:text-2xl m-0 text-indigo-900">
        <slot />
    </h3>
</template>

<script setup lang="ts">
defineProps<{ id: string }>()
</script>
