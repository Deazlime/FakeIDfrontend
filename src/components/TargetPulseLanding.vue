<template>
  <main class="flex overflow-hidden flex-col items-center pb-20 bg-rose-100">
    <TargetPulseHeader />
    <HeroSection />
    <FeaturesSection />
  </main>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TargetPulseHeader from "./TargetPulseHeader.vue";
import HeroSection from "./HeroSection.vue";
import FeaturesSection from "./FeaturesSection.vue";

export default defineComponent({
  name: "TargetPulseLanding",
  components: {
    TargetPulseHeader,
    HeroSection,
    FeaturesSection,
  },
});
</script>
