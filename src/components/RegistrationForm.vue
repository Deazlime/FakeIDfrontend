<template>
  <form
    @submit.prevent="handleSubmit"
    class="flex flex-col w-[430px] max-md:w-full"
  >
    <section class="flex flex-col">
      <h2 class="text-3xl">Зарегистрироваться</h2>
      <div class="mt-6">
        <p class="text-base">Если у вас есть аккаунт</p>
        <p class="mt-1.5">
          <span>Вы можете</span>
          <span class="font-bold text-blue-800">Войти !</span>
        </p>
      </div>
    </section>

    <div class="flex flex-col gap-11 mt-14">
      <FormInput
        id="email"
        label="Email"
        v-model="formData.email"
        placeholder="Введите свой Email"
        input-type="email"
      >
        <template #icon>
          <EmailIcon />
        </template>
      </FormInput>

      <FormInput
        id="username"
        label="Ник"
        v-model="formData.username"
        placeholder="Введите свой ник"
        input-type="text"
      >
        <template #icon>
          <UserIcon />
        </template>
      </FormInput>

      <FormInput
        id="password"
        label="Пароль"
        v-model="formData.password"
        :input-type="showPassword ? 'text' : 'password'"
        placeholder="Введите свой пароль"
      >
        <template #icon>
          <LockIcon />
        </template>
        <template #suffix>
          <button
            type="button"
            class="ml-[10px]"
            @click="showPassword = !showPassword"
          >
            <EyeIcon />
          </button>
        </template>
      </FormInput>

      <FormInput
        id="confirmPassword"
        label="Подтвердить пароль"
        v-model="formData.confirmPassword"
        :input-type="showConfirmPassword ? 'text' : 'password'"
        placeholder="Подтвердите свой пароль"
      >
        <template #icon>
          <LockIcon />
        </template>
        <template #suffix>
          <button
            type="button"
            class="ml-[10px]"
            @click="showConfirmPassword = !showConfirmPassword"
          >
            <EyeIcon />
          </button>
        </template>
      </FormInput>
    </div>

    <button
      type="submit"
      class="py-3.5 mt-14 text-lg text-white bg-orange-600 shadow-lg rounded-[32px]"
    >
      Зарегистрироваться
    </button>
  </form>
</template>

<script setup lang="ts">
import { ref, reactive } from "vue";
import FormInput from "./FormInput.vue";
import EmailIcon from "./Icons/EmailIcon.vue";
import UserIcon from "./Icons/UserIcon.vue";
import LockIcon from "./Icons/LockIcon.vue";
import EyeIcon from "./Icons/EyeIcon.vue";

const showPassword = ref(false);
const showConfirmPassword = ref(false);

const formData = reactive({
  email: "",
  username: "",
  password: "",
  confirmPassword: "",
});

const handleSubmit = () => {
  // Handle form submission
  console.log("Form submitted:", formData);
};
</script>
