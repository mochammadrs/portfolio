<template>
  <section id="about" class="relative py-20 md:py-32 overflow-hidden">
    
    <NuxtImg
      src="~/assets/images/about-splatter.svg"
      alt="Efek kuas cat latar belakang"
      class="absolute z-0 top-[332px] left-[-363px] w-[1010.66px] h-[968.45px] -rotate-[22deg] opacity-20"
    />

    <div class="relative container mx-auto px-4 z-10">
      
      <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
        
        <div class="w-full max-w-sm mx-auto">
          <NuxtImg
            src="~/assets/images/foto-profil.jpg"
            alt="Foto profil"
            class="rounded-lg shadow-2xl w-full h-auto object-cover"
          />
        </div>

        <div>
          <h2 class="text-4xl font-bold mb-4">About Me</h2>
          <p class="text-gray-300 leading-relaxed mb-6">
            Saya adalah seorang Junior Frontend Developer dengan passion untuk menciptakan antarmuka web yang bersih, modern, dan intuitif. Saya selalu bersemangat untuk mempelajari teknologi baru dan berkolaborasi dalam tim untuk menghasilkan produk digital yang luar biasa.
          </p>
          <a
            href="/cv-anda.pdf"
            target="_blank"
            class="inline-block bg-red-600 hover:bg-red-700 text-white font-bold py-3 px-6 rounded-md transition-colors duration-300"
          >
            Download CV
          </a>
        </div>
      </div>
    </div>
  </section>
</template>