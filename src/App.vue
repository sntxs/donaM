<template>
  <div class="min-h-screen bg-white">
    <!-- Navegação -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-white/80 backdrop-blur-md border-b border-gray-100">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
          <div class="flex items-center">
            <div class="flex-shrink-0">
              <h1 class="text-2xl font-bold text-pink-600">DonaM</h1>
            </div>
          </div>
          <div class="hidden md:block">
            <div class="ml-10 flex items-baseline space-x-8">
              <a href="#home"
                class="text-gray-900 hover:text-pink-600 px-3 py-2 rounded-md text-sm font-medium transition-colors">Início</a>
              <a href="#about"
                class="text-gray-900 hover:text-pink-600 px-3 py-2 rounded-md text-sm font-medium transition-colors">Sobre</a>
              <a href="#products"
                class="text-gray-900 hover:text-pink-600 px-3 py-2 rounded-md text-sm font-medium transition-colors">Produtos</a>
              <a href="#gallery"
                class="text-gray-900 hover:text-pink-600 px-3 py-2 rounded-md text-sm font-medium transition-colors">Galeria</a>
              <a href="#contact"
                class="text-gray-900 hover:text-pink-600 px-3 py-2 rounded-md text-sm font-medium transition-colors">Contato</a>
            </div>
          </div>
          <div class="md:hidden">
            <button @click="mobileMenuOpen = !mobileMenuOpen" class="text-gray-900 hover:text-pink-600">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                stroke="currentColor">
                <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16" />
                <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
              </svg>
            </button>
          </div>
        </div>
      </div>

      <!-- Menu mobile -->
      <div v-if="mobileMenuOpen" class="md:hidden">
        <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3 bg-white border-b border-gray-100">
          <a href="#home" @click="mobileMenuOpen = false"
            class="text-gray-900 hover:text-pink-600 block px-3 py-2 rounded-md text-base font-medium">Início</a>
          <a href="#about" @click="mobileMenuOpen = false"
            class="text-gray-900 hover:text-pink-600 block px-3 py-2 rounded-md text-base font-medium">Sobre</a>
          <a href="#products" @click="mobileMenuOpen = false"
            class="text-gray-900 hover:text-pink-600 block px-3 py-2 rounded-md text-base font-medium">Produtos</a>
          <a href="#gallery" @click="mobileMenuOpen = false"
            class="text-gray-900 hover:text-pink-600 block px-3 py-2 rounded-md text-base font-medium">Galeria</a>
          <a href="#contact" @click="mobileMenuOpen = false"
            class="text-gray-900 hover:text-pink-600 block px-3 py-2 rounded-md text-base font-medium">Contato</a>
        </div>
      </div>
    </nav>

    <!-- Conteúdo Principal -->
    <main>
      <!-- Seção Hero -->
      <section id="home" class="pt-24 pb-12 md:pt-32 md:pb-24">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
          <div class="flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-8 md:mb-0">
              <h1 class="text-4xl md:text-6xl font-bold text-gray-900 mb-4">Deliciosas <span
                  class="text-pink-600">Confeitarias</span> para Todas as Ocasiões</h1>
              <p class="text-lg text-gray-600 mb-6">Doces artesanais que trazem alegria para suas celebrações e momentos
                do dia a dia.</p>
              <div class="flex space-x-4">
                <a href="#products"
                  class="bg-pink-600 hover:bg-pink-700 text-white font-medium py-2 px-6 rounded-md transition-colors">Explorar
                  Produtos</a>
                <a href="#contact"
                  class="border border-pink-600 text-pink-600 hover:bg-pink-50 font-medium py-2 px-6 rounded-md transition-colors">Fale
                  Conosco</a>
              </div>
            </div>
            <div class="md:w-1/2">
              <img
                src="https://images.unsplash.com/photo-1587314168485-3236d6710814?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
                alt="Confeitaria sortida" class="rounded-lg shadow-lg w-full h-auto object-cover">
            </div>
          </div>
        </div>
      </section>

      <!-- Seção Sobre -->
      <section id="about" class="py-16 bg-pink-50">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
          <div class="text-center mb-12">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900">Nossa Doce História</h2>
            <div class="w-24 h-1 bg-pink-600 mx-auto mt-4 mb-6"></div>
            <p class="text-lg text-gray-600 max-w-3xl mx-auto">Criando deliciosas confeitarias com paixão e criatividade
              desde 2010.</p>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="bg-white p-6 rounded-lg shadow-md transition-transform hover:scale-105">
              <div class="w-16 h-16 bg-pink-100 rounded-full flex items-center justify-center mb-4 mx-auto">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-pink-600" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M12 6v6m0 0v6m0-6h6m-6 0H6" />
                </svg>
              </div>
              <h3 class="text-xl font-semibold text-gray-900 mb-2">Ingredientes Premium</h3>
              <p class="text-gray-600 text-center">Utilizamos apenas os melhores ingredientes para garantir qualidade e
                sabor excepcionais em cada mordida.</p>
            </div>

            <div class="bg-white p-6 rounded-lg shadow-md transition-transform hover:scale-105">
              <div class="w-16 h-16 bg-pink-100 rounded-full flex items-center justify-center mb-4 mx-auto">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-pink-600" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                </svg>
              </div>
              <h3 class="text-xl font-semibold text-gray-900 mb-2">Feito com Amor</h3>
              <p class="text-gray-600 text-center">Cada confeitaria é cuidadosamente feita à mão com atenção aos
                detalhes e paixão pela perfeição.</p>
            </div>

            <div class="bg-white p-6 rounded-lg shadow-md transition-transform hover:scale-105">
              <div class="w-16 h-16 bg-pink-100 rounded-full flex items-center justify-center mb-4 mx-auto">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-pink-600" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z" />
                </svg>
              </div>
              <h3 class="text-xl font-semibold text-gray-900 mb-2">Criações Inovadoras</h3>
              <p class="text-gray-600 text-center">Exploramos continuamente novos sabores e designs para trazer
                experiências únicas e deliciosas de confeitaria.</p>
            </div>
          </div>

          <div class="mt-16 flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-8 md:mb-0 md:pr-8">
              <img
                src="https://images.unsplash.com/photo-1558961363-fa8fdf82db35?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
                alt="Nossa cozinha de confeitaria" class="rounded-lg shadow-lg w-full h-auto object-cover">
            </div>
            <div class="md:w-1/2">
              <h3 class="text-2xl font-bold text-gray-900 mb-4">Nossa Paixão & Expertise</h3>
              <p class="text-gray-600 mb-4">Fundada pela mestre confeiteira Maria Silva, DonaM começou como um pequeno
                negócio familiar e cresceu para se tornar uma marca querida conhecida por sua qualidade excepcional e
                criatividade.</p>
              <p class="text-gray-600 mb-4">Nossa equipe de artesãos habilidosos combina técnicas tradicionais com
                inovação moderna para criar confeitarias que são não apenas deliciosas, mas visualmente deslumbrantes.
              </p>
              <p class="text-gray-600">Temos orgulho em criar experiências doces memoráveis para casamentos,
                aniversários, eventos corporativos e indulgências do dia a dia.</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Seção de Produtos -->
      <section id="products" class="py-16">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
          <div class="text-center mb-12">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900">Nossos Produtos</h2>
            <div class="w-24 h-1 bg-pink-600 mx-auto mt-4 mb-6"></div>
            <p class="text-lg text-gray-600 max-w-3xl mx-auto">Descubra nossa seleção de doces artesanais feitos com os
              melhores ingredientes e muito amor.</p>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Produto 1 -->
            <div class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105">
              <img
                src="https://images.unsplash.com/photo-1599599810769-bcde5a160d32?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
                alt="Chocolates Artesanais" class="w-full h-64 object-cover">
              <div class="p-6">
                <h3 class="text-xl font-semibold text-gray-900 mb-2">Chocolates Artesanais</h3>
                <p class="text-gray-600 mb-4">Nossos chocolates artesanais são feitos com cacau premium e recheios
                  gourmet que derretem na boca.</p>
                <div class="flex justify-between items-center">
                  <span class="text-pink-600 font-bold">R$25,00 - R$75,00</span>
                  <button
                    class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors">Encomendar</button>
                </div>
              </div>
            </div>

            <!-- Produto 2 -->
            <div class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105">
              <img
                src="https://images.unsplash.com/photo-1528975604071-b4dc52a2d18c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
                alt="Macarons Gourmet" class="w-full h-64 object-cover">
              <div class="p-6">
                <h3 class="text-xl font-semibold text-gray-900 mb-2">Macarons Gourmet</h3>
                <p class="text-gray-600 mb-4">Delicados macarons franceses em uma variedade de sabores vibrantes,
                  perfeitos para qualquer ocasião.</p>
                <div class="flex justify-between items-center">
                  <span class="text-pink-600 font-bold">R$18,00 - R$45,00</span>
                  <button
                    class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors">Encomendar</button>
                </div>
              </div>
            </div>

            <!-- Produto 3 -->
            <div class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105">
              <img
                src="https://images.unsplash.com/photo-1570476922354-d77dbb933a9e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
                alt="Caramelos Especiais" class="w-full h-64 object-cover">
              <div class="p-6">
                <h3 class="text-xl font-semibold text-gray-900 mb-2">Caramelos Especiais</h3>
                <p class="text-gray-600 mb-4">Caramelos macios e saborosos, feitos com manteiga fresca e disponíveis em
                  sabores tradicionais e exclusivos.</p>
                <div class="flex justify-between items-center">
                  <span class="text-pink-600 font-bold">R$15,00 - R$35,00</span>
                  <button
                    class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors">Encomendar</button>
                </div>
              </div>
            </div>

            <!-- Produto 4 -->
            <div class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105">
              <img
                src="https://images.unsplash.com/photo-1551024506-0bccd828d307?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
                alt="Doces Brasileiros" class="w-full h-64 object-cover">
              <div class="p-6">
                <h3 class="text-xl font-semibold text-gray-900 mb-2">Doces Brasileiros</h3>
                <p class="text-gray-600 mb-4">Uma seleção de doces tradicionais brasileiros, incluindo brigadeiros,
                  beijinhos e quindins.</p>
                <div class="flex justify-between items-center">
                  <span class="text-pink-600 font-bold">R$20,00 - R$50,00</span>
                  <button
                    class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors">Encomendar</button>
                </div>
              </div>
            </div>

            <!-- Produto 5 -->
            <div class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105">
              <img
                src="https://images.unsplash.com/photo-1464195244916-405fa0a82545?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
                alt="Tortas Gourmet" class="w-full h-64 object-cover">
              <div class="p-6">
                <h3 class="text-xl font-semibold text-gray-900 mb-2">Tortas Gourmet</h3>
                <p class="text-gray-600 mb-4">Tortas artesanais com sabores sofisticados, perfeitas para celebrações
                  especiais e eventos.</p>
                <div class="flex justify-between items-center">
                  <span class="text-pink-600 font-bold">R$45,00 - R$120,00</span>
                  <button
                    class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors">Encomendar</button>
                </div>
              </div>
            </div>

            <!-- Produto 6 -->
            <div class="bg-white rounded-lg shadow-md overflow-hidden transition-transform hover:scale-105">
              <img
                src="https://images.unsplash.com/photo-1563729784474-d77dbb933a9e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
                alt="Caixas de Presente" class="w-full h-64 object-cover">
              <div class="p-6">
                <h3 class="text-xl font-semibold text-gray-900 mb-2">Caixas de Presente</h3>
                <p class="text-gray-600 mb-4">Caixas elegantes com seleções variadas de nossos doces mais populares, o
                  presente perfeito para qualquer ocasião.</p>
                <div class="flex justify-between items-center">
                  <span class="text-pink-600 font-bold">R$60,00 - R$150,00</span>
                  <button
                    class="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded-md transition-colors">Encomendar</button>
                </div>
              </div>
            </div>
          </div>

          <div class="text-center mt-12">
            <a href="#contact"
              class="inline-block bg-pink-600 hover:bg-pink-700 text-white font-medium py-3 px-8 rounded-md transition-colors">Solicite
              um Orçamento Personalizado</a>
          </div>
        </div>
      </section>

      <!-- Seção de Galeria -->
      <section id="gallery" class="py-16 bg-pink-50">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
          <div class="text-center mb-12">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900">Nossa Galeria</h2>
            <div class="w-24 h-1 bg-pink-600 mx-auto mt-4 mb-6"></div>
            <p class="text-lg text-gray-600 max-w-3xl mx-auto">Uma amostra visual das nossas deliciosas criações
              artesanais.</p>
          </div>

          <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
            <div class="relative overflow-hidden rounded-lg group">
              <img
                src="https://images.unsplash.com/photo-1606312619070-d48b4c652a52?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
                alt="Chocolates"
                class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110">
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                <p class="text-white font-medium p-4">Chocolates Belgas</p>
              </div>
            </div>

            <div class="relative overflow-hidden rounded-lg group">
              <img
                src="https://images.unsplash.com/photo-1558326567-98ae2405596b?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
                alt="Macarons" class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110">
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                <p class="text-white font-medium p-4">Macarons Coloridos</p>
              </div>
            </div>

            <div class="relative overflow-hidden rounded-lg group">
              <img
                src="https://images.unsplash.com/photo-1551404973-761c83cd8339?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
                alt="Torta" class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110">
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                <p class="text-white font-medium p-4">Torta de Frutas Vermelhas</p>
              </div>
            </div>

            <div class="relative overflow-hidden rounded-lg group">
              <img
                src="https://images.unsplash.com/photo-1587314168485-3236d6710814?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
                alt="Doces variados"
                class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110">
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                <p class="text-white font-medium p-4">Seleção de Doces</p>
              </div>
            </div>

            <div class="relative overflow-hidden rounded-lg group">
              <img
                src="https://images.unsplash.com/photo-1612203985729-70726954388c?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
                alt="Brigadeiros"
                class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110">
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                <p class="text-white font-medium p-4">Brigadeiros Gourmet</p>
              </div>
            </div>

            <div class="relative overflow-hidden rounded-lg group">
              <img
                src="https://images.unsplash.com/photo-1550617931-e17a7b70dce2?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
                alt="Cupcakes" class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110">
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                <p class="text-white font-medium p-4">Cupcakes Decorados</p>
              </div>
            </div>

            <div class="relative overflow-hidden rounded-lg group">
              <img
                src="https://images.unsplash.com/photo-1464349095431-e9a21285b5c3?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
                alt="Cookies" class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110">
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                <p class="text-white font-medium p-4">Cookies Artesanais</p>
              </div>
            </div>

            <div class="relative overflow-hidden rounded-lg group">
              <img
                src="https://images.unsplash.com/photo-1514517604298-cf80e0fb7f1e?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
                alt="Doces para festas"
                class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110">
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                <p class="text-white font-medium p-4">Doces para Eventos</p>
              </div>
            </div>
          </div>

          <div class="text-center mt-12">
            <a href="#contact"
              class="inline-block border border-pink-600 text-pink-600 hover:bg-pink-50 font-medium py-3 px-8 rounded-md transition-colors">Solicite
              um Catálogo Completo</a>
          </div>
        </div>
      </section>

      <!-- Seção de Contato -->
      <section id="contact" class="py-16">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
          <div class="text-center mb-12">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900">Fale Conosco</h2>
            <div class="w-24 h-1 bg-pink-600 mx-auto mt-4 mb-6"></div>
            <p class="text-lg text-gray-600 max-w-3xl mx-auto">Entre em contato para encomendas, informações ou para
              discutir suas necessidades especiais.</p>
          </div>

          <div class="flex flex-col md:flex-row bg-white rounded-lg shadow-lg overflow-hidden">
            <div class="md:w-1/2 bg-pink-50 p-8 md:p-12">
              <h3 class="text-2xl font-bold text-gray-900 mb-6">Informações de Contato</h3>

              <div class="flex items-start mb-6">
                <div class="flex-shrink-0 bg-pink-100 rounded-full p-3 mr-4">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-pink-600" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                  </svg>
                </div>
                <div>
                  <h4 class="text-lg font-semibold text-gray-900 mb-1">Endereço</h4>
                  <p class="text-gray-600">Rua das Flores, 123<br>Jardim Primavera<br>São Paulo, SP 01234-567</p>
                </div>
              </div>

              <div class="flex items-start mb-6">
                <div class="flex-shrink-0 bg-pink-100 rounded-full p-3 mr-4">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-pink-600" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                  </svg>
                </div>
                <div>
                  <h4 class="text-lg font-semibold text-gray-900 mb-1">Telefone</h4>
                  <p class="text-gray-600">(11) 5555-1234</p>
                </div>
              </div>

              <div class="flex items-start mb-6">
                <div class="flex-shrink-0 bg-pink-100 rounded-full p-3 mr-4">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-pink-600" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                  </svg>
                </div>
                <div>
                  <h4 class="text-lg font-semibold text-gray-900 mb-1">Email</h4>
                  <p class="text-gray-600">contato@docedelicia.com.br</p>
                </div>
              </div>

              <div class="flex items-start">
                <div class="flex-shrink-0 bg-pink-100 rounded-full p-3 mr-4">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-pink-600" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                </div>
                <div>
                  <h4 class="text-lg font-semibold text-gray-900 mb-1">Horário de Funcionamento</h4>
                  <p class="text-gray-600">Segunda a Sexta: 9h às 18h<br>Sábado: 9h às 14h<br>Domingo: Fechado</p>
                </div>
              </div>

              <div class="mt-8">
                <h4 class="text-lg font-semibold text-gray-900 mb-4">Siga-nos</h4>
                <div class="flex space-x-4">
                  <a href="#" class="text-gray-400 hover:text-pink-500 transition-colors">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                      <path
                        d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z" />
                    </svg>
                  </a>
                  <a href="#" class="text-gray-400 hover:text-pink-500 transition-colors">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                      <path
                        d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z" />
                    </svg>
                  </a>
                  <a href="#" class="text-gray-400 hover:text-pink-500 transition-colors">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                      <path
                        d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z" />
                    </svg>
                  </a>
                </div>
              </div>
            </div>

            <div class="md:w-1/2 p-8 md:p-12">
              <h3 class="text-2xl font-bold text-gray-900 mb-6">Envie sua Mensagem</h3>

              <form>
                <div class="mb-6">
                  <label for="name" class="block text-gray-700 font-medium mb-2">Nome</label>
                  <input type="text" id="name"
                    class="w-full px-4 py-3 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-pink-600 focus:border-transparent"
                    placeholder="Seu nome completo">
                </div>

                <div class="mb-6">
                  <label for="email" class="block text-gray-700 font-medium mb-2">Email</label>
                  <input type="email" id="email"
                    class="w-full px-4 py-3 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-pink-600 focus:border-transparent"
                    placeholder="seu.email@exemplo.com">
                </div>

                <div class="mb-6">
                  <label for="subject" class="block text-gray-700 font-medium mb-2">Assunto</label>
                  <input type="text" id="subject"
                    class="w-full px-4 py-3 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-pink-600 focus:border-transparent"
                    placeholder="Assunto da mensagem">
                </div>

                <div class="mb-6">
                  <label for="message" class="block text-gray-700 font-medium mb-2">Mensagem</label>
                  <textarea id="message" rows="5"
                    class="w-full px-4 py-3 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-pink-600 focus:border-transparent"
                    placeholder="Sua mensagem aqui..."></textarea>
                </div>

                <button type="submit"
                  class="w-full bg-pink-600 hover:bg-pink-700 text-white font-medium py-3 px-6 rounded-md transition-colors">Enviar
                  Mensagem</button>
              </form>
            </div>
          </div>
        </div>
      </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white pt-16 pb-8">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-12">
          <div>
            <h3 class="text-xl font-bold mb-4">DonaM</h3>
            <p class="text-gray-400 mb-4">Criando momentos doces e memoráveis desde 2010. Especialistas em confeitaria
              artesanal para todas as ocasiões.</p>
            <div class="flex space-x-4">
              <a href="#" class="text-gray-400 hover:text-pink-500 transition-colors">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path
                    d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z" />
                </svg>
              </a>
              <a href="#" class="text-gray-400 hover:text-pink-500 transition-colors">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path
                    d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z" />
                </svg>
              </a>
              <a href="#" class="text-gray-400 hover:text-green-500 transition-colors">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 448 512">
                  <path
                    d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z" />
                </svg>
              </a>
            </div>
          </div>

          <div>
            <h3 class="text-xl font-bold mb-4">Links Rápidos</h3>
            <ul class="space-y-2">
              <li><a href="#home" class="text-gray-400 hover:text-pink-500 transition-colors">Início</a></li>
              <li><a href="#about" class="text-gray-400 hover:text-pink-500 transition-colors">Sobre Nós</a></li>
              <li><a href="#products" class="text-gray-400 hover:text-pink-500 transition-colors">Produtos</a></li>
              <li><a href="#gallery" class="text-gray-400 hover:text-pink-500 transition-colors">Galeria</a></li>
              <li><a href="#contact" class="text-gray-400 hover:text-pink-500 transition-colors">Contato</a></li>
            </ul>
          </div>

          <div>
            <h3 class="text-xl font-bold mb-4">Categorias</h3>
            <ul class="space-y-2">
              <li><a href="#" class="text-gray-400 hover:text-pink-500 transition-colors">Chocolates</a></li>
              <li><a href="#" class="text-gray-400 hover:text-pink-500 transition-colors">Macarons</a></li>
              <li><a href="#" class="text-gray-400 hover:text-pink-500 transition-colors">Doces Brasileiros</a></li>
              <li><a href="#" class="text-gray-400 hover:text-pink-500 transition-colors">Tortas</a></li>
              <li><a href="#" class="text-gray-400 hover:text-pink-500 transition-colors">Presentes</a></li>
            </ul>
          </div>

          <div>
            <h3 class="text-xl font-bold mb-4">Contato</h3>
            <ul class="space-y-2">
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-pink-500 mt-0.5" fill="none"
                  viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
                <span class="text-gray-400">Rua das Flores, 123, São Paulo, SP</span>
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-green-500 mt-0.5" fill="currentColor"
                  viewBox="0 0 448 512">
                  <path
                    d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z" />
                </svg>
                <span class="text-gray-400">(11) 98765-4321</span>
              </li>
              <li class="flex items-start">
                <a href="https://wa.me/5511987654321" target="_blank"
                  class="text-gray-400 hover:text-green-500 transition-colors flex items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-green-500 mt-0.5" fill="currentColor"
                    viewBox="0 0 448 512">
                    <path
                      d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z" />
                  </svg>
                  <span>Fale conosco no WhatsApp</span>
                </a>
              </li>
            </ul>
          </div>
        </div>

        <div class="border-t border-gray-800 pt-8">
          <div class="flex flex-col md:flex-row justify-between items-center">
            <p class="text-gray-400 text-sm mb-4 md:mb-0">&copy; 2025 DonaM. Todos os direitos reservados.</p>
            <div class="flex space-x-6">
              <a href="#" class="text-gray-400 hover:text-pink-500 text-sm">Política de Privacidade</a>
              <a href="#" class="text-gray-400 hover:text-pink-500 text-sm">Termos de Serviço</a>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const mobileMenuOpen = ref(false);
</script>

<style>
html {
  scroll-behavior: smooth;
}

body {
  font-family: 'Roboto', sans-serif;
}
</style>