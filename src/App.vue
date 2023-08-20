<script setup>
import {ref} from 'vue'
import ParentComponent from './components/ParentComponent.vue';

const parentMessage = ref('Hello Parent Component')

// const message = reactive({
//   name : 'Jone Doe',
//   age : 50,
//   occupation : 'Web Devolopper',
// })
</script>

<template>
<div class="container mx-auto bg-gray-300">

 <div class="flex flex-col">
  <ParentComponent :message="parentMessage"/>
 </div>
   


</div>
  

</template>

<style scoped>

</style>





