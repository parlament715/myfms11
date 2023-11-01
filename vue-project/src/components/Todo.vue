<script>
import listitem from "./store.vue"
</script>
<template>
<div class="paral">
<listitem v-for="(item, index) in list" :content="item" :key="index"/>
</div>
</template>
<style>
.paral {
    margin: 20px;
    padding: 20px;
    border: 2px solid seagreen;
}
</style>