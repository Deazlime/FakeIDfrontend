<script setup lang="ts">
import LoginForm from "./LoginForm.vue";
import WelcomeSection from "./WelcomeSection.vue";
</script>

<template>
  <main class="overflow-hidden px-8 py-5 bg-rose-100 max-md:px-5">
    <div class="flex gap-5 max-md:flex-col">
      <LoginForm />
      <WelcomeSection />
    </div>
  </main>
</template>
