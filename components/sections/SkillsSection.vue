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
  <section id="skills" class="relative min-h-screen flex items-center py-20 md:py-32">
    <div class="container mx-auto px-12">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
        <div>
          <h2 class="text-5xl font-bold mb-2 text-[#F44336]">Skills</h2>
          <p class="mb-12 max-w-2xl text-[#000C24] text-2xl">
            Saya terus belajar dan mengasah kemampuan saya dalam berbagai teknologi front-end dan back-end untuk
            menciptakan produk yang solid dan modern.
          </p>
        </div>
        <div class="w-full max-w-sm mx-auto md:order-last">
          <img
          src="~/assets/images/bgPoto.svg"
          alt="bg Foto"
          class="absolute top-[90px] left-[1230px] object-cover"
          >
          <img 
          src="~/assets/images/profil.jpg" 
          alt="Foto profil"
          class="relative rounded-lg shadow-2xl w-full h-auto z-10 object-cover"
          >
        <img
          src="~/assets/images/splatterBgSkills.svg"
          alt="splatter bg skills"
          class="absolute top-[590px] left-[1250px] object-cover"
          >
        </div>
      </div>
    </div>
    <div class="absolute px-12 left-3 bottom-[60px]">
      <TheScroll2 />
    </div>
  </section>
</template>