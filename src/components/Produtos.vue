<template>
  <!-- Seção de Produtos -->
  <section id="produtos" class="py-20">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <span class="text-pink-600 font-medium text-sm uppercase tracking-wider"
          >Nossa Seleção</span
        >
        <h2 class="text-3xl md:text-5xl font-bold text-gray-900 mt-2">
          Nossos Produtos
        </h2>
        <div class="w-24 h-1 bg-pink-600 mx-auto mt-4 mb-6"></div>
        <p class="text-lg text-gray-600 max-w-3xl mx-auto">
          Descubra nossa seleção de doces artesanais feitos com os melhores
          ingredientes e muito amor.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Produtos principais (sempre visíveis) -->
        <div 
          v-for="(item, index) in produtosIniciais" 
          :key="`produto-${index}`"
          class="bg-white rounded-xl shadow-lg overflow-hidden transition-all duration-300 hover:shadow-xl group border border-gray-100"
        >
          <div class="relative overflow-hidden h-64">
            <img
              :src="item.imagem"
              :alt="item.titulo"
              class="w-full h-full object-cover transition-transform duration-700"
            />
            <div
              v-if="item.destaque"
              class="absolute top-4 right-4 bg-pink-600 text-white text-xs font-bold px-3 py-1 rounded-full"
            >
              Popular
            </div>
          </div>
          <div class="p-6">
            <h3 class="text-xl font-semibold text-gray-900 mb-2">
              {{ item.titulo }}
            </h3>
            <p class="text-gray-600 mb-4">
              {{ item.descricao }}
            </p>
            <div class="flex justify-between items-center">
              <!-- <span class="text-pink-600 font-bold">R$25,00 - R$75,00</span> -->
              <button
                class="cursor-pointer border-2 border-pink-600 text-pink-600 font-medium py-3 px-8 rounded-full transition-all hover:shadow-md hover:shadow-pink-900/70"
              >
                <a @click="(e) => scrollToSection(e, '#contato')">Encomendar</a>
              </button>
            </div>
          </div>
        </div>

        <!-- Produtos adicionais (com animação) -->
        <transition-group name="produtos-fade" tag="div" class="contents">
          <div 
            v-for="(item, index) in produtosAdicionais" 
            :key="`produto-extra-${index}`"
            class="bg-white rounded-xl shadow-lg overflow-hidden transition-all duration-300 hover:shadow-xl group border border-gray-100"
          >
            <div class="relative overflow-hidden h-64">
              <img
                :src="item.imagem"
                :alt="item.titulo"
                class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
              />
              <div
                v-if="item.destaque"
                class="absolute top-4 right-4 bg-pink-600 text-white text-xs font-bold px-3 py-1 rounded-full"
              >
                Popular
              </div>
            </div>
            <div class="p-6">
              <h3 class="text-xl font-semibold text-gray-900 mb-2">
                {{ item.titulo }}
              </h3>
              <p class="text-gray-600 mb-4">
                {{ item.descricao }}
              </p>
              <div class="flex justify-between items-center">
                <!-- <span class="text-pink-600 font-bold">R$18,00 - R$45,00</span> -->
                <button
                  class="cursor-pointer border-2 border-pink-600 text-pink-600 font-medium py-3 px-8 rounded-full transition-all hover:shadow-md hover:shadow-pink-900/70"
                >
                  <a @click="(e) => scrollToSection(e, '#contato')">Encomendar</a>
                </button>
              </div>
            </div>
          </div>
        </transition-group>
      </div>

      <!-- Botão Ver Mais/Menos com animação -->
      <div class="text-center mt-8">
        <button
          @click="toggleMostrarMais"
          class="cursor-pointer border-2 border-pink-600 text-pink-600 font-medium py-1 px-4 rounded-full transition-all hover:shadow-md hover:shadow-pink-900/70 transform hover:scale-105 duration-300"
        >
          <span class="inline-flex items-center">
            {{ mostrarTodos ? "Ver Menos" : "Ver Mais" }}
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4 ml-2 transition-transform duration-300"
              :class="mostrarTodos ? 'rotate-180' : ''"
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
          @click="(e) => scrollToSection(e, '#contato')"
          class="inline-block bg-pink-600 hover:bg-pink-700 text-white font-medium py-3 px-8 rounded-full shadow-md transition-all hover:shadow-pink-900/70 cursor-pointer"
          >Solicite um Orçamento Personalizado</a
        >
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, computed } from "vue";

// Array com todos os produtos
const todosProdutos = [
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860164/bolo-de-pote_kfa0va.jpg",
    titulo: "Bolo de Pote",
    descricao: "Delicioso bolo em camadas, perfeito para consumir a qualquer hora. Disponível em diversos sabores como chocolate, morango e baunilha.",
    destaque: true
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860164/churros_uu2arq.jpg",
    titulo: "Churros Gourmet",
    descricao: "Churros crocantes por fora e macios por dentro, recheados com doce de leite ou chocolate. Uma delícia irresistível!",
    destaque: false
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860163/IMG_5707_jejtbc.jpg",
    titulo: "Cake Box",
    descricao: "Caixa com seleção de doces tradicionais e mini bolos, perfeita para compartilhar momentos doces com quem você ama.",
    destaque: true
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860160/doce-de-taca_x2duxq.jpg",
    titulo: "Doce de Taça",
    descricao: "Sobremesas em taças com camadas harmoniosas de creme, frutas e biscoitos. Elegante e perfeito para impressionar convidados.",
    destaque: false
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860160/ninho-com-nutella2_h3eloc.jpg",
    titulo: "Ninho com Nutella",
    descricao: "A combinação perfeita do leite Ninho cremoso com a indulgência da Nutella. Um dos nossos best-sellers que conquista todos os paladares.",
    destaque: true
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860159/bolo-caseiro_ere5ja.jpg",
    titulo: "Bolo Caseiro",
    descricao: "Bolos caseiros feitos com carinho e ingredientes selecionados. O gostinho de infância que traz memórias afetivas.",
    destaque: false
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860159/doce-de-leite_tcyref.jpg",
    titulo: "Doce de Leite Artesanal",
    descricao: "Doce de leite cremoso feito no fogão à lenha, seguindo a tradição. Perfeito para comer puro ou usar em outras sobremesas.",
    destaque: false
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860159/cake-box3_mxyh8v.jpg",
    titulo: "Cake Box Premium",
    descricao: "Caixa especial com mini bolos e doces variados. Uma experiência completa de sabores, ideal para presente ou degustação.",
    destaque: true
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860158/brigadeiro-gourmet_suvyq8.jpg",
    titulo: "Brigadeiro Gourmet",
    descricao: "Brigadeiros artesanais em diversas versões, desde o tradicional até sabores exclusivos como café, pistache e frutas vermelhas.",
    destaque: false
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860158/cake-box2_cihwbt.jpg",
    titulo: "Cake Box Especial",
    descricao: "Seleção especial de doces finos em uma caixa elegante, perfeita para presentear em datas comemorativas.",
    destaque: false
  },
  {
    imagem: "https://res.cloudinary.com/dgbo657qq/image/upload/v1742860157/bicho-de-pe_e7kena.jpg",
    titulo: "Bicho de Pé",
    descricao: "Docinho com delicado sabor de morango, coberto com açúcar cristal. Clássico da confeitaria brasileira com nosso toque especial.",
    destaque: false
  }
];

// Quantidade inicial de produtos a mostrar
const quantidadeInicial = 6;

// Estado para controlar se mostra todos os produtos ou não
const mostrarTodos = ref(false);

// Computed property para os produtos iniciais (sempre visíveis)
const produtosIniciais = computed(() => {
  return todosProdutos.slice(0, quantidadeInicial);
});

// Computed property para os produtos adicionais (que serão animados)
const produtosAdicionais = computed(() => {
  return mostrarTodos.value ? todosProdutos.slice(quantidadeInicial) : [];
});

// Função para alternar entre mostrar mais/menos produtos
const toggleMostrarMais = () => {
  mostrarTodos.value = !mostrarTodos.value;
};

// Função para rolar até uma seção específica
const scrollToSection = (event, sectionId) => {
  event.preventDefault();
  const section = document.querySelector(sectionId);
  if (section) {
    section.scrollIntoView({ behavior: "smooth" });
  }
};
</script>

<style scoped>
/* Animações para os produtos */
.produtos-fade-enter-active,
.produtos-fade-leave-active {
  transition: all 0.5s ease;
}

.produtos-fade-enter-from {
  opacity: 0;
  transform: translateY(30px);
}

.produtos-fade-leave-to {
  opacity: 0;
  transform: translateY(30px);
}

/* Garante que os itens apareçam com tempos levemente diferentes */
.produtos-fade-enter-from:nth-child(2n) {
  transition-delay: 0.1s;
}

.produtos-fade-enter-from:nth-child(3n) {
  transition-delay: 0.2s;
}

.produtos-fade-enter-from:nth-child(4n) {
  transition-delay: 0.3s;
}

/* Para o componente "contents" */
.contents {
  display: contents;
}
</style>
