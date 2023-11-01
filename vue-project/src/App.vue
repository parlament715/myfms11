<template>
   <div>
      <div class="header" :class="{ 'red-header': isActive }">ToDo</div>
   </div>
   <ToDo @myActivate="isActive = true" @myDeactivate="isActive = false" />
</template>

<script setup>
import ToDo from '@/components/ToDo.vue'
import { ref } from 'vue'

const isActive = ref(false)
</script>

<style>
.header {
   font-size: 32px;
}

.text {
   margin-top: 10px;
   margin-bottom: 10px;
}

.red-header {
   color: red;
   font-weight: bold;
}
</style>
