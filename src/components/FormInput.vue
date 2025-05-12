<template>
  <div class="flex flex-col">
    <label :for="id" class="text-sm text-neutral-400">{{ label }}</label>
    <div
      class="flex items-center pb-2 mt-3"
      :class="[
        focused || modelValue ? 'border-slate-900' : 'border-neutral-400',
        'border-2',
      ]"
    >
      <div class="mr-[11px]">
        <slot name="icon"></slot>
      </div>
      <input
        :id="id"
        :type="inputType"
        :value="modelValue"
        @input="
          $emit('update:modelValue', ($event.target as HTMLInputElement).value)
        "
        @focus="focused = true"
        @blur="focused = false"
        :placeholder="placeholder"
        class="w-full text-base bg-transparent text-slate-900"
      />
      <slot name="suffix"></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

defineProps<{
  id: string;
  label: string;
  modelValue: string;
  placeholder: string;
  inputType: string;
}>();

defineEmits<{
  (e: "update:modelValue", value: string): void;
}>();

const focused = ref(false);
</script>
