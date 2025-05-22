<template>
  <div class="flask-message">
    <h2>Message from Flask Backend</h2>
    <div v-if="loading" class="loading">Loading...</div>
    <div v-else-if="error" class="error">{{ error }}</div>
    <div v-else class="message">{{ message }}</div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';
import { fetchHello } from '../services/api';

const message = ref('');
const loading = ref(true);
const error = ref('');

onMounted(async () => {
  try {
    const data = await fetchHello();
    message.value = data.message;
  } catch (err) {
    error.value = 'Failed to connect to the backend server. Is it running?';
  } finally {
    loading.value = false;
  }
});
</script>

<style scoped>
.flask-message {
  margin: 20px;
  padding: 20px;
  border-radius: 8px;
  background-color: #f5f5f5;
  max-width: 500px;
}

.loading {
  color: #666;
}

.error {
  color: #ff4d4f;
}

.message {
  color: #52c41a;
  font-size: 1.5em;
  font-weight: bold;
}
</style> 