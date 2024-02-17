<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Email</th>
          <!-- Otros campos -->
        </tr>
      </thead>
      <tbody>
        <tr v-for="user in users" :key="user.id">
          <td>{{ user.name }}</td>
          <td>{{ user.email }}</td>
          <!-- Otros campos -->
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const users = ref([
  { id: 1, name: 'John Doe', email: 'john@example.com' },
  { id: 2, name: 'Jane Smith', email: 'jane@example.com' },
  // Agrega más usuarios genéricos aquí
]);
</script>
