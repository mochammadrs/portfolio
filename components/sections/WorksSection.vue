<script lang="ts" setup>

import { Splide, SplideSlide } from '@splidejs/vue-splide';

import '@splidejs/splide/dist/css/splide.min.css';


const options = {
  type       : 'loop', 
  perPage    : 1,      
  autoplay   : true,   
  interval   : 5000,   
  arrows     : true,   
  pagination : true,   
};

const projects = [
  {
    id: 1,
    title: 'Simon Game',
    description: 'An inquisitive Computer Science Engineering student, skilled in leadership, seeking to leverage solid development skills with focus on collaboration, communication and passion.',
    image: 'https://images.unsplash.com/photo-1526925539332-aa3b66e35444?q=80&w=765&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D', // Ganti dengan path gambar Anda
    tags: ['HTML5', 'CSS3', 'JavaScript', 'ReactJS'],
    githubUrl: 'https://github.com/username/simon-game',
  },
  {
    id: 2,
    title: 'Project Beta',
    description: 'Deskripsi singkat untuk Project Beta, fokus pada fitur-fitur utamanya dan teknologi yang digunakan.',
    image: 'https://images.unsplash.com/photo-1509966756634-9c23dd6e6815?q=80&w=776&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
    tags: ['Vue.js', 'Nuxt.js', 'Tailwind CSS'],
    githubUrl: 'https://github.com/username/project-beta',
  },
];
</script>

<template>
  <section id="works" class="relative min-h-screen flex items-center py-20 md:py-32">
    <div class="container mx-auto px-12">
        <img
          src="~/assets/images/bgPoto.svg"
          alt="bg Foto"
          class="absolute top-[80px] left-[-10px] object-cover"
          > 
        <img
          src="~/assets/images/splatterBgSkills.svg"
          alt="splatter bg skills"
          class="absolute top-[520px] left-[-10px] w-[313] object-cover"
          >
      <Splide :options="options" aria-label="My Favorite Projects">
        <SplideSlide v-for="project in projects" :key="project.id">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
            <div>
              <NuxtImg :src="project.image" :alt="project.title" class="relative rounded-lg shadow-2xl w-[450px] h-auto object-cover"/> 
            </div>
            <div>
              <h2 class="text-5xl font-bold mb-2 text-[#F44336]">Works</h2>
              <h3 class="text-3xl font-semibold mb-4 text-[#F44336]">{{ project.title }}</h3>
              <p class="text-[#000C24] text-2xl leading-relaxed mb-8">{{ project.description }}</p>
              <div class="flex flex-wrap gap-3 mb-8">
                <span v-for="tag in project.tags" :key="tag" class="bg-gray-700 text-gray-300 text-sm font-semibold px-4 py-2 rounded-md">
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
      <div class="absolute px-12 left-3 bottom-[60px]">
        <TheScroll2/>
      </div>
    </div>
  </section>
</template>

<style>

.splide__pagination__page {
  background: #4A5568; 
  width: 25%;
  height: 4px;
  border-radius: 2px;
  margin: 0 8px;
  transition: background 0.3s;
}

.splide__pagination__page.is-active {
  background: #E53E3E; 
  transform: scale(1);
}


.splide__pagination__page .splide__sr {
  display: none;
}
</style>