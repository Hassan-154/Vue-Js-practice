<script setup>
import { ref } from 'vue';
// import StoreData from './components/StoreData.vue';
import RefPractice from './components/RefPractice.vue'
const username = 'Haman Ali';

const receivedEmail = ref('');
const handleEmailSent = (email) => {
  receivedEmail.value = email;
};
</script>

<template>
  <div>
    <!-- <StoreData :username="username" @emailSent="handleEmailSent" /> -->
    <p>Received Email: {{ receivedEmail }}</p>
  </div>
  <!-- useRef practice -->
  <RefPractice/>
</template>

<style scoped>

</style>
