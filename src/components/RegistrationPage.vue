<template>
  <main class="flex w-full bg-rose-100 min-h-[screen]">
    <div class="flex px-11 py-8 w-full max-md:px-6 max-sm:px-4">
      <div class="flex flex-col w-full">
        <header class="flex items-center">
          <Logo />
        </header>
        <div class="flex gap-32 mt-20 w-full max-md:flex-col max-md:gap-10">
          <RegistrationForm />
          <WelcomePanel />
        </div>
      </div>
    </div>
  </main>
</template>

<script setup lang="ts">
import Logo from "./Logo.vue";
import RegistrationForm from "./RegistrationForm.vue";
import WelcomePanel from "./WelcomePanel.vue";
</script>
