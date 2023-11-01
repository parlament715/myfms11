<!-- eslint-disable vue/multi-word-component-names -->
<template>
   <div class="paral">
      <ListItem v-for="(item, index) in list" :content="item" :key="index" />
      <hr />
      <div class="button" @mouseover="emit('myActivate')" @mouseleave="emit('myDeactivate')">
         Add
      </div>
   </div>
</template>

<script setup>
import ListItem from './ListItem.vue'
import { reactive } from 'vue'

const emit = defineEmits(['myActivate', 'myDeactivate'])

const list = reactive(['gshdjfkgkjasdhgfk', 'gadshjfgajsdfhg', 'rwtyqur qwvrEY'])
</script>

<style>
.paral {
   margin: 20px;
   padding: 20px;
   border: 2px solid seagreen;
}

.button {
   width: 150px;
   height: 30px;
   line-height: 30px;
   border: 1px solid #ccc;
   border-radius: 4px;
   background-color: #f3f6f9;
   text-align: center;
}

.button:hover {
   cursor: pointer;
   background-color: #fff;
   box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.15);
}
</style>
