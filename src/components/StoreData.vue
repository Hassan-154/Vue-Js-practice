<template>
  <div>
    <p>prop received from parent component</p>
    <p>{{ username }}</p>
    <input v-model="selectedUsername" placeholder="Enter email" />
    <button @click="sendEmail">Send Email</button>
  </div>
</template>
<script setup>

import { ref, defineProps, defineEmits, onMounted } from "vue";

const props = defineProps(["username"]);
const emits = defineEmits(["emailSent"]);
const selectedUsername = ref("");

onMounted(() => {
  selectedUsername.value = props.username;
});

const sendEmail = () => {
  emits("emailSent", selectedUsername.value);
};

</script>
