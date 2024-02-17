<template>
  <main>
    <form @submit.prevent="login">
      <h1>Login</h1>
      <input v-model="email" type="email" placeholder="Email Address" />
      <input v-model="password" type="password" placeholder="Password" />
      <button type="submit">Login</button>
    </form>
  </main>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const email = ref('user@correo.com'); 
const password = ref('1234'); 
const login = () => {
  if (email.value === 'user@correo.com' && password.value === '1234') {
    alert('Inicio de sesión exitoso.');
  } else {
    alert('Credenciales incorrectas. Inténtalo de nuevo.');
  }
};
</script>