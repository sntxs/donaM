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
        <div v-for="(item, index) in primeirasImagens" :key="`fixed-${index}`"
          class="relative overflow-hidden rounded-lg group">
          <img :src="item.imagem" :alt="item.titulo"
            class="w-full h-80 object-cover transition-transform duration-500 group-hover:scale-110" />
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
            <p class="text-white font-medium p-4">{{ item.titulo }}</p>
          </div>
        </div>

        <!-- Imagens adicionais que recebem animação -->
        <transition-group name="gallery-fade" tag="div" class="contents">
          <div v-for="(item, index) in imagensAdicionais" :key="`extra-${index}`"
            class="relative overflow-hidden rounded-lg group">
            <img :src="item.imagem" :alt="item.titulo"
              class="w-full h-80 object-cover transition-transform duration-500 group-hover:scale-110" />
            <div
              class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
              <p class="text-white font-medium p-4">{{ item.titulo }}</p>
            </div>
          </div>
        </transition-group>
      </div>

      <!-- Botão Ver Mais/Menos com animação -->
      <div class="text-center mt-8">
        <button @click="toggleMostrarMais"
          class="cursor-pointer border-2 border-pink-600 text-pink-600 font-medium py-1 px-6 rounded-full transition-all hover:shadow-md hover:shadow-pink-900/70 transform hover:scale-105 duration-300">
          <span class="inline-flex items-center">
            {{ mostrarTodas ? "Ver Menos" : "Ver Mais" }}
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-2 transition-transform duration-300"
              :class="mostrarTodas ? 'rotate-180' : ''" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </span>
        </button>
      </div>

      <div class="text-center mt-4">
        <a href="https://api.whatsapp.com/send?phone=5518981453272&text=Olá+Dona+M,+tudo+bem%3F+Gostaria+que+me+enviasse+todo+o+seu+catálogo+😃&fbclid=PAZXh0bgNhZW0CMTEAAaYjqYz14GPzMY_rKxcyeXQutg6oD-rkevEHq9v9ZSUplG_kisaVC58fwhQ_aem_WXtmUGnCamVQeX-B-S82RA"
          target="_blank"
          class="inline-block bg-pink-600 hover:bg-pink-700 text-white font-medium py-3 px-8 rounded-full shadow-md transition-all hover:shadow-pink-900/70 cursor-pointer">Solicite
          um Catálogo Completo</a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from "vue";

// Array com as URLs das imagens do Cloudinary
const todasImagens = [
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860103/IMG_0212_rdtood.jpg",
    titulo: "Bolo Decorativo"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860106/IMG_1552_a4vrco.jpg",
    titulo: "Bolo de Aniversário"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860104/IMG_2846_djmr8c.jpg",
    titulo: "Bolo Diferenciado"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860107/IMG_3370_ddjmbl.jpg",
    titulo: "Bolo Especial"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860107/IMG_4286_hpyrpd.jpg",
    titulo: "Bolo Quadrado"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860111/IMG_4640_ngofen.jpg",
    titulo: "Bolo Especial"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860105/IMG_5326_qx16lu.jpg",
    titulo: "Bolo de Aniversário"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860108/IMG_5436_jkeo2m.jpg",
    titulo: "Bolo Exclusivo"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860108/IMG_5578_uvrw07.jpg",
    titulo: "Bolo de Aniversário"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860113/IMG_6034_szxed4.jpg",
    titulo: "Bolo de Aniversário"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860109/IMG_6756_lidio7.jpg",
    titulo: "Bolo de Chocolate"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860114/IMG_6867_tr5gxr.jpg",
    titulo: "Bolo Especial"
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860116/IMG_9540_rst6mo.jpg",
    titulo: "Bolo de Aniversário"
  },
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
