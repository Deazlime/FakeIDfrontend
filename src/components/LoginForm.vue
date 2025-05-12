<script setup lang="ts">
import BrandLogo from "./BrandLogo.vue";
import FormInput from "./FormInput.vue";

const email = ref("");
const password = ref("");
const rememberMe = ref(false);

const handleSubmit = () => {
  // Handle form submission
  console.log({
    email: email.value,
    password: password.value,
    rememberMe: rememberMe.value,
  });
};
</script>

<template>
  <section class="w-[41%] max-md:ml-0 max-md:w-full">
    <div class="flex flex-col mt-2.5 max-md:mt-10 max-md:max-w-full">
      <BrandLogo class="self-start" />

      <form
        @submit.prevent="handleSubmit"
        class="flex flex-col items-start pl-20 mt-24 w-full max-md:pl-5 max-md:mt-10 max-md:max-w-full"
      >
        <h2 class="text-3xl font-medium text-black max-md:ml-0.5">Войти</h2>
        <p class="mt-6 text-base text-black max-md:ml-0.5">
          Если у вас нет аккаунта
        </p>
        <p class="mt-1.5 text-base text-black max-md:ml-0.5">
          Вы можете
          <span class="font-semibold text-[#0C21C1]">Зарегистрироваться !</span>
        </p>

        <FormInput
          v-model="email"
          label="Email"
          type="email"
          icon="https://cdn.builder.io/api/v1/image/assets/TEMP/2a65a50a59989d2690e99cb1d8e71c23d95a25f3?placeholderIfAbsent=true&apiKey=54e2ce62783f4d88b7e90980390d388c"
          class="mt-14 w-full"
        />

        <FormInput
          v-model="password"
          label="Пароль"
          type="password"
          icon="https://cdn.builder.io/api/v1/image/assets/TEMP/6a64a1c780b2bfdecae3288a71a48d37f7d6e525?placeholderIfAbsent=true&apiKey=54e2ce62783f4d88b7e90980390d388c"
          show-password-toggle
          class="mt-12"
        />

        <div
          class="flex gap-10 mt-4 w-full text-xs font-light max-md:max-w-full"
        >
          <label
            class="flex flex-1 gap-2.5 text-black whitespace-nowrap items-center cursor-pointer"
          >
            <input
              type="checkbox"
              v-model="rememberMe"
              class="w-[15px] h-[15px] border border-black"
            />
            <span>Запомнить</span>
          </label>
          <button type="button" class="text-neutral-600">
            Забыли пароль ?
          </button>
        </div>

        <button
          type="submit"
          class="px-16 py-3.5 mt-16 text-lg font-medium text-white whitespace-nowrap bg-orange-600 rounded-[32px] shadow-[0px_4px_26px_rgba(0,0,0,0.25)] max-md:px-5 max-md:mt-10 max-md:max-w-full"
        >
          Войти
        </button>

        <p class="self-center mt-9 ml-10 text-base font-medium text-zinc-400">
          или продолжить с
        </p>

        <img
          src="https://cdn.builder.io/api/v1/image/assets/TEMP/2a866a9b451feb01a9fa405d9f1591da344fb2a9?placeholderIfAbsent=true&apiKey=54e2ce62783f4d88b7e90980390d388c"
          alt="Social login options"
          class="object-contain self-center mt-9 ml-10 max-w-full aspect-[3.83] w-[165px]"
        />
      </form>
    </div>
  </section>
</template>
