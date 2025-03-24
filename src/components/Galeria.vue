<template>
  <!-- Seção de Galeria -->
  <section id="galeria" class="py-16 bg-pink-50">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900">
          Nossa Galeria
        </h2>
        <div class="w-24 h-1 bg-pink-600 mx-auto mt-4 mb-6"></div>
        <p class="text-lg text-gray-600 max-w-3xl mx-auto">
          Uma amostra visual das nossas deliciosas criações artesanais.
        </p>
      </div>

      <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
        <!-- Imagens que sempre são mostradas (as primeiras 8) -->
        <div
          v-for="(item, index) in primeirasImagens"
          :key="`fixed-${index}`"
          class="relative overflow-hidden rounded-lg group"
        >
          <img
            :src="item.imagem"
            :alt="item.titulo"
            class="w-full h-80 object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white font-medium p-4">{{ item.titulo }}</p>
          </div>
        </div>

        <!-- Imagens adicionais que recebem animação -->
        <transition-group name="gallery-fade" tag="div" class="contents">
          <div
            v-for="(item, index) in imagensAdicionais"
            :key="`extra-${index}`"
            class="relative overflow-hidden rounded-lg group"
          >
            <img
              :src="item.imagem"
              :alt="item.titulo"
              class="w-full h-80 object-cover transition-transform duration-500 group-hover:scale-110"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
            >
              <p class="text-white font-medium p-4">{{ item.titulo }}</p>
            </div>
          </div>
        </transition-group>
      </div>

      <!-- Botão Ver Mais/Menos com animação -->
      <div class="text-center mt-8">
        <button
          @click="toggleMostrarMais"
          class="cursor-pointer border-2 border-pink-600 text-pink-600 font-medium py-1 px-6 rounded-full transition-all hover:shadow-md hover:shadow-pink-900/70 transform hover:scale-105 duration-300"
        >
          <span class="inline-flex items-center">
            {{ mostrarTodas ? "Ver Menos" : "Ver Mais" }}
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4 ml-2 transition-transform duration-300"
              :class="mostrarTodas ? 'rotate-180' : ''"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M19 9l-7 7-7-7"
              />
            </svg>
          </span>
        </button>
      </div>

      <div class="text-center mt-4">
        <a
          href="https://api.whatsapp.com/send?phone=5518981453272&text=Olá+Dona+M,+tudo+bem%3F+Gostaria+que+me+enviasse+todo+o+seu+catálogo+😃&fbclid=PAZXh0bgNhZW0CMTEAAaYjqYz14GPzMY_rKxcyeXQutg6oD-rkevEHq9v9ZSUplG_kisaVC58fwhQ_aem_WXtmUGnCamVQeX-B-S82RA"
          target="_blank"
          class="inline-block bg-pink-600 hover:bg-pink-700 text-white font-medium py-3 px-8 rounded-full shadow-md transition-all hover:shadow-pink-900/70 cursor-pointer"
          >Solicite um Catálogo Completo</a
        >
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from "vue";

// Importar todas as imagens
import img0212 from "../assets/galeria/IMG_0212.jpg";
import img1552 from "../assets/galeria/IMG_1552.jpg";
import img2846 from "../assets/galeria/IMG_2846.jpg";
import img3370 from "../assets/galeria/IMG_3370.jpg";
import img4286 from "../assets/galeria/IMG_4286.jpg";
import img4640 from "../assets/galeria/IMG_4640.jpg";
import img5326 from "../assets/galeria/IMG_5326.jpg";
import img5436 from "../assets/galeria/IMG_5436.jpg";
import img5578 from "../assets/galeria/IMG_5578.jpg";
import img6034 from "../assets/galeria/IMG_6034.jpg";
import img6756 from "../assets/galeria/IMG_6756.jpg";
import img6867 from "../assets/galeria/IMG_6867.jpg";
import img9540 from "../assets/galeria/IMG_9540.jpg";

const todasImagens = [
  { imagem: img0212, titulo: "Bolo Decorativo" },
  { imagem: img1552, titulo: "Bolo de Aniversário" },
  { imagem: img2846, titulo: "Bolo Diferenciado" },
  { imagem: img3370, titulo: "Bolo Especial" },
  { imagem: img4286, titulo: "Bolo Quadrado" },
  { imagem: img4640, titulo: "Bolo Especial" },
  { imagem: img5326, titulo: "Bolo de Aniversário" },
  { imagem: img5436, titulo: "Bolo Exclusivo" },
  { imagem: img5578, titulo: "Bolo de Aniversário" },
  { imagem: img6034, titulo: "Bolo de Aniversário" },
  { imagem: img6756, titulo: "Bolo de Chocolate" },
  { imagem: img6867, titulo: "Bolo Especial" },
  { imagem: img9540, titulo: "Bolo de Aniversário" },
];

// Quantidade inicial de imagens a mostrar
const quantidadeInicial = 4;

// Estado para controlar se mostra todas as imagens ou não
const mostrarTodas = ref(false);

// Computed property para as primeiras imagens (sempre visíveis)
const primeirasImagens = computed(() => {
  return todasImagens.slice(0, quantidadeInicial);
});

// Computed property para as imagens adicionais (que serão animadas)
const imagensAdicionais = computed(() => {
  return mostrarTodas.value ? todasImagens.slice(quantidadeInicial) : [];
});

// Função para alternar entre mostrar mais/menos imagens
const toggleMostrarMais = () => {
  mostrarTodas.value = !mostrarTodas.value;
};
</script>

<style scoped>
/* Animações para a galeria */
.gallery-fade-enter-active,
.gallery-fade-leave-active {
  transition: all 0.5s ease;
}

.gallery-fade-enter-from {
  opacity: 0;
  transform: translateY(30px);
}

.gallery-fade-leave-to {
  opacity: 0;
  transform: translateY(30px);
}

/* Garante que os itens apareçam com tempos levemente diferentes */
.gallery-fade-enter-from:nth-child(2n) {
  transition-delay: 0.1s;
}

.gallery-fade-enter-from:nth-child(3n) {
  transition-delay: 0.2s;
}

.gallery-fade-enter-from:nth-child(4n) {
  transition-delay: 0.3s;
}

/* Para o componente "contents" */
.contents {
  display: contents;
}
</style>
