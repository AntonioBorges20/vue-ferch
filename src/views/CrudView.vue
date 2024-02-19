<template>
  <div class="crud-view">
    <table>
      <thead>
        <tr>
          <th class="th-color">Name</th>
          <th class="th-color">Email</th>
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

<style scoped>
.crud-view {
  margin: 20px;
} 

table {
  width: 100%;
  border-collapse: collapse;
}

th, td {
  padding: 10px;
  text-align: left;
  border-bottom: 1px solid #ddd;
}

th {
  background-color: #f2f2f2;
}

.th-color {
  background-color: #007bff;
  color: #fff;
}
</style>

