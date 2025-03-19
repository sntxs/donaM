// @ts-nocheck
<template>
  <div class="min-h-screen bg-white">
    <!-- Navegação -->
    <nav
      class="fixed top-0 left-0 right-0 z-50 bg-white/80 backdrop-blur-md border-b border-gray-100 shadow-sm"
    >
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
          <div class="flex items-center">
            <div class="flex-shrink-0">
              <h1 class="text-2xl font-bold text-pink-600 font-script">
                Dona M - Confeitaria
              </h1>
            </div>
          </div>
          <div class="hidden md:block">
            <div class="ml-10 flex items-baseline space-x-8">
              <a
                @click="(e) => scrollToSection(e, '#home')"
                class="text-gray-900 hover:text-pink-600 px-3 py-2 rounded-md text-sm font-medium transition-colors cursor-pointer"
                >Início</a
              >
              <a
                @click="(e) => scrollToSection(e, '#sobre')"
                class="text-gray-900 hover:text-pink-600 px-3 py-2 rounded-md text-sm font-medium transition-colors cursor-pointer"
                >Sobre</a
              >
              <a
                @click="(e) => scrollToSection(e, '#produtos')"
                class="text-gray-900 hover:text-pink-600 px-3 py-2 rounded-md text-sm font-medium transition-colors cursor-pointer"
                >Produtos</a
              >
              <a
                @click="(e) => scrollToSection(e, '#galeria')"
                class="text-gray-900 hover:text-pink-600 px-3 py-2 rounded-md text-sm font-medium transition-colors cursor-pointer"
                >Galeria</a
              >
              <a
                @click="(e) => scrollToSection(e, '#contato')"
                class="text-gray-900 hover:text-pink-600 px-3 py-2 rounded-md text-sm font-medium transition-colors cursor-pointer"
                >Contato</a
              >
            </div>
          </div>
          <div class="md:hidden">
            <button
              @click="mobileMenuOpen = !mobileMenuOpen"
              class="text-gray-900 hover:text-pink-600"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-6 w-6"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  v-if="!mobileMenuOpen"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                />
                <path
                  v-else
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M6 18L18 6M6 6l12 12"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>

      <!-- Menu mobile -->
      <div v-if="mobileMenuOpen" class="md:hidden">
        <div
          class="px-2 pt-2 pb-3 space-y-1 sm:px-3 bg-white border-b border-gray-100"
        >
          <a
            @click="(e) => { scrollToSection(e, '#home'); mobileMenuOpen = false; }"
            class="text-gray-900 hover:text-pink-600 block px-3 py-2 rounded-md text-base font-medium cursor-pointer"
            >Início</a
          >
          <a
            @click="(e) => { scrollToSection(e, '#sobre'); mobileMenuOpen = false; }"
            class="text-gray-900 hover:text-pink-600 block px-3 py-2 rounded-md text-base font-medium cursor-pointer"
            >Sobre</a
          >
          <a
            @click="(e) => { scrollToSection(e, '#produtos'); mobileMenuOpen = false; }"
            class="text-gray-900 hover:text-pink-600 block px-3 py-2 rounded-md text-base font-medium cursor-pointer"
            >Produtos</a
          >
          <a
            @click="(e) => { scrollToSection(e, '#galeria'); mobileMenuOpen = false; }"
            class="text-gray-900 hover:text-pink-600 block px-3 py-2 rounded-md text-base font-medium cursor-pointer"
            >Galeria</a
          >
          <a
            @click="(e) => { scrollToSection(e, '#contato'); mobileMenuOpen = false; }"
            class="text-gray-900 hover:text-pink-600 block px-3 py-2 rounded-md text-base font-medium cursor-pointer"
            >Contato</a
          >
        </div>
      </div>
    </nav>

    <Hero />
    <Sobre />
    <Produtos />
    <Galeria />
    <Contato />
    <Footer />

    <!-- Botão Voltar ao Topo -->
    <button
      @click="scrollToTop"
      @mousedown="buttonPressed = true"
      @mouseup="buttonPressed = false"
      @mouseleave="buttonPressed = false"
      class="fixed bottom-6 right-6 bg-pink-600 hover:bg-pink-700 text-white p-3 rounded-full shadow-lg transition-all duration-300 z-50 transform"
      :class="{
        'opacity-0 pointer-events-none': !showBackToTop,
        'opacity-100': showBackToTop,
        'scale-90': buttonPressed,
        'scale-100': !buttonPressed,
      }"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-6 w-6"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M5 15l7-7 7 7"
        />
      </svg>
    </button>
  </div>
</template>

<script setup lang="ts">
import Hero from "./components/Hero.vue";
import Sobre from "./components/Sobre.vue";
import Produtos from "./components/Produtos.vue";
import Galeria from "./components/Galeria.vue";
import Contato from "./components/Contato.vue";
import Footer from "./components/Footer.vue";
import { ref, onMounted, onUnmounted } from "vue";

const mobileMenuOpen = ref(false);
const showBackToTop = ref(false);
const buttonPressed = ref(false);

const scrollToSection = (event, sectionId) => {
  event.preventDefault();
  const section = document.querySelector(sectionId);
  if (section) {
    section.scrollIntoView({ behavior: 'smooth' });
  }
};

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
};

const checkScroll = () => {
  showBackToTop.value = window.scrollY > 300;
};

onMounted(() => {
  window.addEventListener("scroll", checkScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", checkScroll);
});
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Dancing+Script:wght@600&display=swap");

html {
  scroll-behavior: smooth;
}

::-webkit-scrollbar {
  width: 12px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
  background: #e83e8c;
  border-radius: 5px;
}

::-webkit-scrollbar-thumb:hover {
  background: #d6336c;
}

body {
  font-family: "Poppins", sans-serif;
}

.font-script {
  font-family: "Dancing Script", cursive;
}
</style>
