<template>
    <h2 class="font-bold">Details Form</h2>
    <FormComponent @formSubmitted="handleFormSubmitted" />
    <DisplayComponent :userDetails="userData" />
</template>

<script setup>
import { ref } from 'vue';
import DisplayComponent from './components/DisplayComponent.vue';
import FormComponent from './components/FormComponent.vue';

const userData = ref({});

function handleFormSubmitted(formData) {
  userData.value = formData;
  // console.log('FormDetails', userData.value);
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline {
  text-decoration: underline;
}

.success {
  color: green;
}

.promoted {
  font-style: italic;
}

.new {
  color: green;
}

.soldout {
  color: red;
}

</style>
