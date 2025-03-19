<template>
  <!-- Seção de Produtos -->
  <section id="products" class="py-20">
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
        <!-- Produto 1 -->
        <div
          class="bg-white rounded-xl shadow-lg overflow-hidden transition-all duration-300 hover:shadow-xl group border border-gray-100"
        >
          <div class="relative overflow-hidden h-64">
            <img
              src="https://images.unsplash.com/photo-1599599810769-bcde5a160d32?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
              alt="Chocolates Artesanais"
              class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
            />
            <div
              class="absolute top-4 right-4 bg-pink-600 text-white text-xs font-bold px-3 py-1 rounded-full"
            >
              Popular
            </div>
          </div>
          <div class="p-6">
            <h3 class="text-xl font-semibold text-gray-900 mb-2">
              Chocolates Artesanais
            </h3>
            <p class="text-gray-600 mb-4">
              Nossos chocolates artesanais são feitos com cacau premium e
              recheios gourmet que derretem na boca.
            </p>
            <div class="flex justify-between items-center">
              <!-- <span class="text-pink-600 font-bold">R$25,00 - R$75,00</span> -->
              <button
                class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-5 rounded-full transition-all hover:shadow-md transform hover:-translate-y-1"
              >
              <a @click="(e) => scrollToSection(e, '#contact')">Encomendar</a>
              </button>
            </div>
          </div>
        </div>

        <!-- Produto 2 -->
        <div
          class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105"
        >
          <img
            src="https://images.unsplash.com/photo-1528975604071-b4dc52a2d18c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
            alt="Macarons Gourmet"
            class="w-full h-64 object-cover"
          />
          <div class="p-6">
            <h3 class="text-xl font-semibold text-gray-900 mb-2">
              Macarons Gourmet
            </h3>
            <p class="text-gray-600 mb-4">
              Delicados macarons franceses em uma variedade de sabores
              vibrantes, perfeitos para qualquer ocasião.
            </p>
            <div class="flex justify-between items-center">
              <!-- <span class="text-pink-600 font-bold">R$18,00 - R$45,00</span> -->
              <button
                class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors"
              >
                <a @click="(e) => scrollToSection(e, '#contact')">Encomendar</a>
              </button>
            </div>
          </div>
        </div>

        <!-- Produto 3 -->
        <div
          class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105"
        >
          <img
            src="https://images.unsplash.com/photo-1612203985729-70726954388c?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
            alt="Caramelos Especiais"
            class="w-full h-64 object-cover"
          />
          <div class="p-6">
            <h3 class="text-xl font-semibold text-gray-900 mb-2">
              Caramelos Especiais
            </h3>
            <p class="text-gray-600 mb-4">
              Caramelos macios e saborosos, feitos com manteiga fresca e
              disponíveis em sabores tradicionais e exclusivos.
            </p>
            <div class="flex justify-between items-center">
              <!-- <span class="text-pink-600 font-bold">R$15,00 - R$35,00</span> -->
              <button
                class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors"
              >
                <a @click="(e) => scrollToSection(e, '#contact')">Encomendar</a> 
              </button>
            </div>
          </div>
        </div>

        <!-- Produto 4 -->
        <div
          class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105"
        >
          <img
            src="https://images.unsplash.com/photo-1551024506-0bccd828d307?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
            alt="Doces Brasileiros"
            class="w-full h-64 object-cover"
          />
          <div class="p-6">
            <h3 class="text-xl font-semibold text-gray-900 mb-2">
              Doces Brasileiros
            </h3>
            <p class="text-gray-600 mb-4">
              Uma seleção de doces tradicionais brasileiros, incluindo
              brigadeiros, beijinhos e quindins.
            </p>
            <div class="flex justify-between items-center">
              <!-- <span class="text-pink-600 font-bold">R$20,00 - R$50,00</span> -->
              <button
                class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors"
              >
              <a @click="(e) => scrollToSection(e, '#contact')">Encomendar</a>
              </button>
            </div>
          </div>
        </div>

        <!-- Produto 5 -->
        <div
          class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105"
        >
          <img
            src="https://images.unsplash.com/photo-1464195244916-405fa0a82545?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
            alt="Tortas Gourmet"
            class="w-full h-64 object-cover"
          />
          <div class="p-6">
            <h3 class="text-xl font-semibold text-gray-900 mb-2">
              Tortas Gourmet
            </h3>
            <p class="text-gray-600 mb-4">
              Tortas artesanais com sabores sofisticados, perfeitas para
              celebrações especiais e eventos.
            </p>
            <div class="flex justify-between items-center">
              <!-- <span class="text-pink-600 font-bold">R$45,00 - R$120,00</span> -->
              <button
                class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors"
              >
              <a @click="(e) => scrollToSection(e, '#contact')">Encomendar</a>
              </button>
            </div>
          </div>
        </div>

        <!-- Produto 6 -->
        <div
          class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105"
        >
          <img
            src="https://images.unsplash.com/photo-1563729784474-d77dbb933a9e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
            alt="Caixas de Presente"
            class="w-full h-64 object-cover"
          />
          <div class="p-6">
            <h3 class="text-xl font-semibold text-gray-900 mb-2">
              Caixas de Presente
            </h3>
            <p class="text-gray-600 mb-4">
              Caixas elegantes com seleções variadas de nossos doces mais
              populares, o presente perfeito para qualquer ocasião.
            </p>
            <div class="flex justify-between items-center">
              <!-- <span class="text-pink-600 font-bold">R$60,00 - R$150,00</span> -->
              <button
                class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors"
              >
                <a @click="(e) => scrollToSection(e, '#contact')">Encomendar</a>
              </button>
            </div>
          </div>
        </div>
      </div>

      <div class="text-center mt-16">
        <a
          @click="(e) => scrollToSection(e, '#contact')"
          class="inline-block bg-pink-600 hover:bg-pink-700 text-white font-medium py-3 px-8 rounded-full shadow-md transition-all hover:shadow-pink-900/70 cursor-pointer"
          >Solicite um Orçamento Personalizado</a
        >
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
