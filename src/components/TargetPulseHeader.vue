<template>
  <header
    class="flex flex-wrap gap-5 justify-between self-stretch py-5 pr-8 w-full bg-rose-100 rounded-lg shadow-[0px_4px_4px_rgba(73,38,29,0.25)] max-md:pr-5"
  >
    <h1 class="my-auto text-xl font-bold text-yellow-950">
      <span style="color: rgba(251, 77, 0, 1)">Target</span>
      <span
        style="
          font-weight: 800;
          font-style: italic;
          color: rgba(202, 231, 247, 1);
        "
        >Pulse</span
      >
    </h1>

    <nav
      class="flex gap-8 items-start text-base font-medium text-rose-100 whitespace-nowrap"
    >
      <button
        class="px-2.5 pt-3 pb-1 bg-orange-600 rounded-lg shadow-[0px_4px_4px_rgba(73,38,29,0.25)]"
      >
        Регистрация
      </button>
      <img
        src="https://cdn.builder.io/api/v1/image/assets/TEMP/c10e6a3df3599ebe0d973d4673ce8993e10a4a7e?placeholderIfAbsent=true&apiKey=54e2ce62783f4d88b7e90980390d388c"
        alt="Navigation Image"
        class="object-contain shrink-0 max-w-full aspect-[3] shadow-[0px_4px_4px_rgba(73,38,29,0.25)] w-[120px]"
      />
    </nav>
  </header>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TargetPulseHeader",
});
</script>
