<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Email</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="user in users" :key="user.id">
          <td>{{ user.name }}</td>
          <td>{{ user.email }}</td>

        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const users = ref([
  { id: 1, name: 'Antonio', email: 'antonio@correo.com' },
  { id: 2, name: 'Misael', email: 'misael@correo.com' },
  { id: 3, name: 'Osmar', email: 'osmar@correo.com' },
  { id: 4, name: 'Jair', email: 'jair@correo.com' },
  { id: 5, name: 'Julio', email: 'julio@correo.com' },
  { id: 6, name: 'Pablo', email: 'pablo@correo.com' },
]);
</script>
