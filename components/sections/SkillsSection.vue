<script lang="ts" setup>
// Definisikan daftar skill Anda di sini
// const skills = [
//   { name: 'HTML', percentage: 95 },
//   { name: 'CSS & Tailwind', percentage: 90 },
//   { name: 'JavaScript', percentage: 80 },
//   { name: 'Vue.js / Nuxt', percentage: 85 },
//   { name: 'React', percentage: 70 },
//   { name: 'Node.js', percentage: 60 },
//   { name: 'Figma', percentage: 75 },
// ];
</script>

<template>
  <section id="skills" class="relative min-h-screen flex flex-col justify-center py-20 md:py-32">
    <div class="container mx-auto px-12">
      <h2 class="text-5xl font-bold mb-2 text-[#F44336]">Skills</h2>
      <p class="mb-12 max-w-2xl text-[#000C24] text-2xl">
        Saya terus belajar dan mengasah kemampuan saya dalam berbagai teknologi front-end dan back-end untuk menciptakan produk yang solid dan modern.
      </p>
      
      <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-7 gap-8">
        <!-- <SkillsCircle 
          v-for="skill in skills" 
          :key="skill.name" 
          :skill="skill"
        /> -->
      </div>
    </div>
        <div class="absolute px-12 left-3 bottom-[60px]">
        <TheScroll2/>
      </div>
  </section>
</template>