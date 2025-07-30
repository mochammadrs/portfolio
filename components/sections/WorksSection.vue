<script lang="ts" setup>
import { Splide, SplideSlide } from '@splidejs/vue-splide';

import '@splidejs/splide/dist/css/splide.min.css';


const options = {
  type: 'loop',
  perPage: 1,
  autoplay: true,
  interval: 5000,
  arrows: true,
  pagination: true,
};

const projects = [
  {
    id: 1,
    title: 'Penicillisolver',
    description: 'Aplikasi lintas platform yang ditujukan untuk membantu dokter dalam menganalisis tren resistensi bakteri.',
    image: 'https://images.unsplash.com/photo-1526925539332-aa3b66e35444?q=80&w=765&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D', // Ganti dengan path gambar Anda
    tags: ['NextJs', 'Python', 'JavaScript', 'CSS', 'Firebase'],
    githubUrl: 'https://github.com/Shua24/penicillisolver',
  },
  {
    id: 2,
    title: 'ReadyNotes',
    description: 'aplikasi web untuk membuat catatan pribadi yang dirancang dengan antarmuka modern, cepat, dan minimalis.',
    image: 'https://images.unsplash.com/photo-1509966756634-9c23dd6e6815?q=80&w=776&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    tags: ['NuxtJs', 'VueJs', 'Tailwind CSS', 'MySql'],
    githubUrl: 'https://github.com/mochammadrs/ReadyNotes',
  },
];
</script>

<template>
  <section id="works" class="relative min-h-screen flex items-center py-20 px-4 md:py-32">
    <div class="container mx-auto">
      <Splide :options="options" aria-label="My Favorite Projects">
        <SplideSlide v-for="project in projects" :key="project.id">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-12 md:gap-0 items-center">
            <div class="flex justify-center md:justify-start relative md:left-5">
              <NuxtImg 
              :src="project.image" :alt="project.title"
                class="relative md:left-[100px] shadow-2xl w-[250px] md:w-[400px] h-auto object-cover z-20 md:[clip-path:polygon(0%_0%,100%_0%,100%_90%,0%_100%)]" />
              <img 
              src="~/assets/images/bgPoto.svg" alt="bg Foto"
                class="absolute top-[-50px] left-[55px] object-cover hidden md:block">
              <img 
              src="~/assets/images/splatterBgWorks.svg" alt="splatter bg Works"
                class="absolute top-[300px] left-[-20px] w-[150px] object-cover hidden md:block">
            </div>
            <div class="relative text-center md:text-left md:right-[50px]">
              <h2 class="text-4xl md:text-5xl font-bold mb-2 text-[#F44336]">Works</h2>
              <h3 class="text-2xl md:text-3xl font-semibold mb-4 text-[#F44336]">{{ project.title }}</h3>
              <p class="text-[#000C24] text-lg md:text-2xl leading-relaxed mb-8">{{ project.description }}</p>
              <div class="flex flex-wrap gap-3 mb-8 justify-center md:justify-start">
                <span 
                v-for="tag in project.tags" :key="tag"
                  class="bg-gray-700 text-gray-300 text-sm font-semibold px-4 py-2 rounded-md">
                  {{ tag }}
                </span>
              </div>
              <a :href="project.githubUrl" target="_blank" class="text-gray-400 hover:text-white transition-colors">
                <Icon name="mdi:github" class="text-4xl" />
              </a>
            </div>
          </div>
        </SplideSlide>
      </Splide>
      <div class="absolute bottom-[10px] md:bottom-[60px] left-1/2 -translate-x-1/2 md:translate-x-3 md:left-12">
        <TheScroll2 />
      </div>
    </div>
  </section>
</template>