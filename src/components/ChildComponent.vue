<script setup>

import { ref, defineEmits } from 'vue';
const props = defineProps({
  message: String
});

// Error message show in console 
// like emit is not defined
// then Solution
const emit = defineEmits(['messageEmitted'])


const emitMessage = () => {
  const customMessage = `Custom message!!`;
  // Emits the event through the provided context
  emit('messageEmitted', customMessage);

};

</script>

<template>

<div class=" p-4 rounded shadow">
    <h2 class="text-lg font-semibold mb-2">Child Component</h2>
    <p class="mb-2">Message from Parent:</p>
    <p class="bg-white p-2 rounded shadow">{{ message }}</p>
    <button class="mt-4 bg-blue-500 text-white px-4 py-2 rounded" 
    @click="emitMessage">Emit Message</button>
  </div>


        
            


    
</template>

<style scoped>

</style>