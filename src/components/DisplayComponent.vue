<template>
    <div class="flex justify-center items-center h-full mb-4">
    <div class="shadow-md border rounded p-4">
      <h2 class="mb-4 font-bold">Show Form Details</h2>
      <div><strong>First Name:</strong>{{ userDetails.firstName }}</div>
      <div><strong>Last Name:</strong>{{ userDetails.lastName }}</div>
      <div><strong>Address:</strong>{{ userDetails.address }}</div>
      <div><strong>City:</strong>{{ userDetails.city }}</div>
      <div><strong>State:</strong>{{ userDetails.state }}</div>
      <div><strong>Zip:</strong>{{ userDetails.zip }}</div>
    </div>
  </div>
</template>

<script setup>

import { defineProps } from 'vue';

// Define props received from the parent component
const props = defineProps({
    userDetails: Object
});

console.log(props.userDetails);


</script>