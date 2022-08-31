<template>
    <h4 :id="id" class="font-extrabold text-lg md:text-xl m-0 text-indigo-900">
        <slot />
    </h4>
</template>

<script setup lang="ts">
defineProps<{ id: string }>()
</script>
