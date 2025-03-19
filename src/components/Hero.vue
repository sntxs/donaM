<template>
  <!-- Seção Hero -->
  <section
    id="home"
    class="pt-24 pb-12 md:pt-32 md:pb-24 bg-gradient-to-b from-pink-50 to-white"
  >
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex flex-col md:flex-row items-center">
        <div class="md:w-1/2 mb-8 md:mb-0">
          <h1 class="text-4xl md:text-6xl font-bold text-gray-900 mb-4">
            Deliciosas
            <span class="text-pink-600 font-script">Confeitarias</span> para
            Todas as Ocasiões
          </h1>
          <p class="text-lg text-gray-600 mb-8">
            Doces artesanais que trazem alegria para suas celebrações e momentos
            do dia a dia, feitos com
            <span class="text-pink-600 font-medium">amor e dedicação</span>.
          </p>
          <div
            class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4"
          >
            <a
              @click="(e) => scrollToSection(e, '#products')"
              class="cursor-pointer bg-pink-600 hover:bg-pink-700 text-white font-medium py-3 px-8 rounded-full shadow-md transition-all hover:shadow-lg transform hover:-translate-y-1"
              >Explorar Produtos</a
            >
            <a
              @click="(e) => scrollToSection(e, '#contact')"
              class="cursor-pointer border-2 border-pink-600 text-pink-600 font-medium py-3 px-8 rounded-full transition-all hover:shadow-md hover:shadow-pink-900/70"
              >Fale Conosco</a
            >
          </div>
        </div>
        <div class="md:w-1/2">
          <div class="relative">
            <div
              class="absolute -inset-4 bg-pink-200 rounded-full opacity-30 blur-xl"
            ></div>
            <img
              src="https://images.unsplash.com/photo-1587314168485-3236d6710814?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
              alt="Confeitaria sortida"
              class="relative rounded-xl shadow-xl w-full h-auto object-cover"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const scrollToSection = (event, sectionId) => {
  event.preventDefault();
  const section = document.querySelector(sectionId);
  if (section) {
    section.scrollIntoView({ behavior: "smooth" });
  }
};
</script>
