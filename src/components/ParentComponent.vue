<script setup>
 import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';
defineProps(['message'])

const receivedMessage = ref('');
  
const MessageEmitted = (message) => {
    receivedMessage.value = message;
  };
</script>

<template>
    <div>
        <h2 class="bg-blue-500 p-5 text-white rounded-md">Parent Component</h2>
     <p>{{ message }}</p>

     <ChildComponent :message="message"  @messageEmitted="MessageEmitted"/>
     <p class="mt-4 p-5 bg-red-500 font-bold text-white">Received message from Child: {{ receivedMessage }}</p>

     
      
    </div>






</template>

<style scoped>

</style>


  

  