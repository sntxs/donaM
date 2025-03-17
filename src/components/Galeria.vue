<template>
  <!-- Seção de Galeria -->
  <section id="gallery" class="py-16 bg-pink-50">
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
        <div class="relative overflow-hidden rounded-lg group">
          <img
            src="https://images.unsplash.com/photo-1606312619070-d48b4c652a52?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
            alt="Chocolates"
            class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white font-medium p-4">Chocolates Belgas</p>
          </div>
        </div>

        <div class="relative overflow-hidden rounded-lg group">
          <img
            src="https://images.unsplash.com/photo-1558326567-98ae2405596b?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
            alt="Macarons"
            class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white font-medium p-4">Macarons Coloridos</p>
          </div>
        </div>

        <div class="relative overflow-hidden rounded-lg group">
          <img
            src="https://images.unsplash.com/photo-1551404973-761c83cd8339?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
            alt="Torta"
            class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white font-medium p-4">Torta de Frutas Vermelhas</p>
          </div>
        </div>

        <div class="relative overflow-hidden rounded-lg group">
          <img
            src="https://images.unsplash.com/photo-1587314168485-3236d6710814?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
            alt="Doces variados"
            class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white font-medium p-4">Seleção de Doces</p>
          </div>
        </div>

        <div class="relative overflow-hidden rounded-lg group">
          <img
            src="https://images.unsplash.com/photo-1612203985729-70726954388c?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
            alt="Brigadeiros"
            class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white font-medium p-4">Brigadeiros Gourmet</p>
          </div>
        </div>

        <div class="relative overflow-hidden rounded-lg group">
          <img
            src="https://images.unsplash.com/photo-1550617931-e17a7b70dce2?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
            alt="Cupcakes"
            class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white font-medium p-4">Cupcakes Decorados</p>
          </div>
        </div>

        <div class="relative overflow-hidden rounded-lg group">
          <img
            src="https://images.unsplash.com/photo-1499636136210-6f4ee915583e?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
            alt="Cookies"
            class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white font-medium p-4">Cookies Artesanais</p>
          </div>
        </div>

        <div class="relative overflow-hidden rounded-lg group">
          <img
            src="https://images.unsplash.com/photo-1514517604298-cf80e0fb7f1e?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
            alt="Doces para festas"
            class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white font-medium p-4">Doces para Eventos</p>
          </div>
        </div>
      </div>

      <div class="text-center mt-12">
        <a
          href="#contact"
          class="inline-block border border-pink-600 text-pink-600 hover:bg-pink-50 font-medium py-3 px-8 rounded-md transition-colors"
          >Solicite um Catálogo Completo</a
        >
      </div>
    </div>
  </section>
</template>
