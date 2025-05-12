<template>
  <section class="w-full max-w-[1128px] max-md:max-w-full">
    <div class="flex gap-5 max-md:flex-col">
      <div class="w-[42%] max-md:ml-0 max-md:w-full">
        <h2
          class="text-6xl font-bold text-yellow-950 max-md:mt-10 max-md:text-4xl"
        >
          Работайте вместе, как никогда раньше
        </h2>
      </div>
      <div class="ml-5 w-[58%] max-md:ml-0 max-md:w-full">
        <img
          src="https://cdn.builder.io/api/v1/image/assets/TEMP/4a4f8f005399639179db91b767d7d66b99d4c824?placeholderIfAbsent=true&apiKey=54e2ce62783f4d88b7e90980390d388c"
          alt="Collaboration Illustration"
          class="object-contain grow mt-10 w-full aspect-[2.08] shadow-[0px_4px_4px_rgba(0,0,0,0.25)] max-md:max-w-full"
        />
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "HeroSection",
});
</script>
