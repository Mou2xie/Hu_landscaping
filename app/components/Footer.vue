<script lang="ts" setup>
const currentYear = new Date().getFullYear();
</script>

<template>
    <footer class=" text-center h-20 bg-slate-600 flex items-center justify-center">
        <p>© {{ currentYear }} Waterloo Carpentry & Outdoors. All rights reserved.</p>
    </footer>
</template>