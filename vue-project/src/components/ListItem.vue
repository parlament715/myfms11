<template>
   <div class="list-item">{{ content }}</div>
</template>

<script setup>
defineProps(['content'])
</script>

<style>
.list-item {
   color: red;
}
</style>
