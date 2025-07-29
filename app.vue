<template>
  <div class="max-w-[1920px] mx-auto">
    <NuxtLayout>
      <div class="relative">
        <img
        src="~/assets/images/splatter.svg"
        alt="Efek kuas cat home"
        class="hidden lg:block absolute top-0 object-cover">
        <HeroSection />
        <img
        src="~/assets/images/splatter2.svg"
        alt="Efek kuas cat about"
        class="hidden lg:block absolute top-[450px] object-cover">
        <AboutMe />
        <img
        src="~/assets/images/splatter3.svg"
        alt="Efek kuas cat about skills"
        class="hidden lg:block absolute top-[1014px] right-0 object-cover">
        <SkillsSection />
        <WorksSection />
        <ContactSection />
      </div>
    </NuxtLayout>
  </div>
</template>

<style>
* {
  font-family: "League Spartan", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
}
</style>
