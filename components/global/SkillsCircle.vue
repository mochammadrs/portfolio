<script lang="ts" setup>
import { computed } from 'vue';

// Komponen ini menerima object 'skill' sebagai properti
const props = defineProps({
  skill: {
    type: Object,
    required: true,
    default: () => ({ name: 'Skill', percentage: 0 }),
  },
});

const radius = 50;
const circumference = 2 * Math.PI * radius;

// Hitung offset stroke berdasarkan persentase untuk membuat efek progress
const strokeOffset = computed(() => {
  return circumference - (props.skill.percentage / 100) * circumference;
});
</script>

<template>
  <div class="flex flex-col items-center gap-2 text-center">
    <div class="relative w-32 h-32">
      <svg class="w-full h-full transform -rotate-90" viewBox="0 0 120 120">
        <circle
          class="text-gray-700"
          stroke-width="10"
          stroke="currentColor"
          fill="transparent"
          :r="radius"
          cx="60"
          cy="60"
        />
        <circle
          class="text-cyan-400"
          stroke-width="10"
          :stroke-dasharray="circumference"
          :stroke-dashoffset="strokeOffset"
          stroke-linecap="round"
          stroke="currentColor"
          fill="transparent"
          :r="radius"
          cx="60"
          cy="60"
        />
      </svg>
      <span class="absolute text-xl font-bold inset-0 flex items-center justify-center">
        {{ skill.percentage }}%
      </span>
    </div>
    <p class="font-semibold mt-2">{{ skill.name }}</p>
  </div>
</template>