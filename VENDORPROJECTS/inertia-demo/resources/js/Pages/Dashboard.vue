<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head, usePage } from '@inertiajs/vue3';

const page = usePage()
const user = page.props.auth.user

const notifications = page.props.notifications

console.log(user)
</script>

<template>
  <div>
    <h1>Welcome, {{ user.name }}</h1>
    <ul>
      <li v-for="note in notifications" :key="note">{{ note }}</li>
    </ul>
  </div>
</template>
