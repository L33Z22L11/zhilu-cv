<script setup lang="ts">
defineProps<{
    to?: string
}>()
</script>

<template>
<NuxtLink
    :to
    un-text="blue-600 @dark:blue-300 print:blue-700 hover:op-80"
    :target="isExtLink(to) ? '_blank' : undefined"
>
    <slot>{{ trimLink(to) }}</slot>
</NuxtLink>
</template>
