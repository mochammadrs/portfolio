<script lang="ts" setup>
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import '@splidejs/splide/dist/css/splide-core.min.css';

const skillCategories = [
  {
    category: 'Languages & Core Tech',
    skills: [
      { name: 'HTML', icon: 'logos:html-5' },
      { name: 'CSS', icon: 'logos:css-3' },
      { name: 'JavaScript', icon: 'logos:javascript' },
      { name: 'Python', icon: 'logos:python' },
    ]
  },
  {
    category: 'Design & Prototyping',
    skills: [
      { name: 'Figma', icon: 'logos:figma' },
    ]
  },
  {
    category: 'Frameworks',
    skills: [
      { name: 'NuxtJs', icon: 'logos:nuxt-icon' },
      { name: 'NextJs', icon: 'logos:nextjs-icon' },
    ]
  },
  {
    category: 'Database & Tools',
    skills: [
      { name: 'MySql', icon: 'logos:mysql' },
      { name: 'Firebase', icon: 'logos:firebase-icon' },
    ]
  },
]

const options = {
  type: 'loop',
  perPage: 1,
  arrows: true,
  pagination: true
};
</script>

<template>
  <section id="skills" class="relative min-h-screen flex items-center py-20 px-4 md:px-12">
    <div class="container mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 md:gap-16 items-center">
        <div class="text-center md:text-left flex flex-col py-12">
          <h2 class="text-4xl md:text-5xl font-bold mb-2 text-[#F44336]">Skills</h2>
          <p class="mb-12 max-w-2xl mx-auto md:mx-0 text-[#000C24] text-lg md:text-2xl">
            Saya terus belajar dan mengasah kemampuan saya dalam berbagai teknologi front-end dan back-end untuk
            menciptakan produk yang solid dan modern.
          </p>
          <div>
          <Splide :options="options" aria-label="My Skills">
            <SplideSlide v-for="category in skillCategories" :key="category.category">
              <div class="text-center p-6">
                <h3 class="text-3xl font-bold text-[#F44336] mb-8">
                  {{ category.category }}
                </h3>
                <div class="flex flex-wrap gap-2 justify-center">
                  <div v-for="skill in category.skills" :key="skill.name" class="flex flex-col items-center gap-2 p-2 rounded w-28">
                    <Icon :name="skill.icon" class="text-3xl"/>
                    <span class="text-[#000C24] text-lg">{{ skill.name }}</span>
                  </div>
                </div>
              </div>
            </SplideSlide>
          </Splide>
        </div>
        </div>
        <div class="relative w-full max-w-xs sm:max-w-sm mx-auto md:order-last">
          <img
          src="~/assets/images/bgPoto.svg"
          alt="bg Foto"
          class="absolute top-[-35px] left-[280px] object-cover hidden md:block"
          >
          <img 
          src="https://images.unsplash.com/photo-1551033406-611cf9a28f67?q=80&w=687&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" 
          alt="Foto profil"
          class="relative shadow-2xl w-full h-auto z-10 object-cover hidden md:block md:[clip-path:polygon(0%_0%,100%_0%,100%_100%,0%_90%)]"
          >
        <img
          src="~/assets/images/splatterBgSkills.svg"
          alt="splatter bg skills"
          class="absolute top-[505px] left-[305px] object-cover hidden md:block"
          >
        </div>
      </div>
    </div>
    <div class="absolute bottom-[10px] md:bottom-[60px] left-1/2 -translate-x-1/2 md:translate-x-3 md:left-12">
      <TheScroll2 />
    </div>
  </section>
</template>

<style>
  .splide__pagination__page {
    background: #4A5568;
    width: 50px;
    height: 5px;
    margin-top: 100px;
    border-radius: 2px;
    transition: background 0.3s;
  }
  
  .splide__pagination__page.is-active {
    background: #F44336;
    transform: scale(1);
  }
  
  .splide__pagination__page .splide__sr {
    display: none;
  }
</style>