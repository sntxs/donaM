<template>
  <!-- Footer -->
  <footer class="bg-gray-900 text-white pt-20 pb-8">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-12">
        <!-- Coluna 1 -->
        <div>
          <!-- <h3 class="text-xl font-bold mb-4 font-script">Dona M Confeitaria</h3> -->
          <img
            src="../assets/logo-donam.jpg"
            alt="Dona M Logo"
            class="h-14 w-14 mb-4 rounded-full"
          />
          <p class="text-gray-400 mb-4">
            Criando momentos doces e memoráveis desde 2019. Especialistas em
            confeitaria artesanal para todas as ocasiões.
          </p>
          <div class="flex space-x-4">
            <a
              href="https://www.instagram.com/donamconfeitaria?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw=="
              class="text-gray-400 hover:text-pink-500 transition-colors instagram"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-6 w-6"
                fill="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"
                />
              </svg>
            </a>
            <a
              href="https://api.whatsapp.com/send?phone=5518981453272&text=Olá+Dona+M,+tudo+bem%3F+😃&fbclid=PAZXh0bgNhZW0CMTEAAaYjqYz14GPzMY_rKxcyeXQutg6oD-rkevEHq9v9ZSUplG_kisaVC58fwhQ_aem_WXtmUGnCamVQeX-B-S82RA"
              class="text-gray-400 hover:text-green-500 transition-colors"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-6 w-6"
                fill="currentColor"
                viewBox="0 0 448 512"
              >
                <path
                  d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"
                />
              </svg>
            </a>
          </div>
        </div>

        <!-- Coluna 2 -->
        <div>
          <h3 class="text-xl font-bold mb-4">Links Rápidos</h3>
          <ul class="space-y-2">
            <li>
              <a
                @click="(e) => scrollToSection(e, '#home')"
                class="text-gray-400 hover:text-pink-500 transition-colors cursor-pointer"
                >Início</a
              >
            </li>
            <li>
              <a
                @click="(e) => scrollToSection(e, '#sobre')"
                class="text-gray-400 hover:text-pink-500 transition-colors cursor-pointer"
                >Sobre Nós</a
              >
            </li>
            <li>
              <a
                @click="(e) => scrollToSection(e, '#produtos')"
                class="text-gray-400 hover:text-pink-500 transition-colors cursor-pointer"
                >Produtos</a
              >
            </li>
            <li>
              <a
                @click="(e) => scrollToSection(e, '#galeria')"
                class="text-gray-400 hover:text-pink-500 transition-colors cursor-pointer"
                >Galeria</a
              >
            </li>
            <li>
              <a
                @click="(e) => scrollToSection(e, '#contato')"
                class="text-gray-400 hover:text-pink-500 transition-colors cursor-pointer"
                >Contato</a
              >
            </li>
          </ul>
        </div>

        <!-- Coluna 3 -->
        <div>
          <h3 class="text-xl font-bold mb-4">Contato</h3>
          <ul class="space-y-2">
            <li class="flex items-start">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5 mr-2 text-pink-500 mt-0.5"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
                />
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
                />
              </svg>
              <span class="text-gray-400">
                Rua Francisco Ruiz Morales, 276 <br />
                Parque São Matheus <br />
                Presidente Prudente, SP
              </span>
            </li>
            <li class="flex items-start">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5 mr-2 text-green-500 mt-0.5"
                fill="currentColor"
                viewBox="0 0 448 512"
              >
                <path
                  d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"
                />
              </svg>
              <a
                href="https://api.whatsapp.com/send?phone=5518981453272&text=Olá+Dona+M,+tudo+bem%3F+😃&fbclid=PAZXh0bgNhZW0CMTEAAaYjqYz14GPzMY_rKxcyeXQutg6oD-rkevEHq9v9ZSUplG_kisaVC58fwhQ_aem_WXtmUGnCamVQeX-B-S82RA"
                target="_blank"
                class="text-gray-400"
              >
                <span class="text-gray-400">(18) 98145-3272</span>
              </a>
            </li>
          </ul>
        </div>
      </div>

      <!-- Rodapé atualizado -->
      <div class="border-t border-gray-800 pt-8 mt-12">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <div class="flex flex-col items-center md:items-start mb-4 md:mb-0">
            <p class="text-gray-400 text-sm">
              &copy; {{ new Date().getFullYear() }} DonaM. Todos os direitos
              reservados.
            </p>
            <p class="text-gray-500 text-xs mt-1">
              Desenvolvido por
              <a
                href="https://nata-portfolio.vercel.app"
                target="_blank"
                class="hover:text-pink-400 transition-colors"
                >© {{ new Date().getFullYear() }} NR.dev</a
              >
            </p>
          </div>
          <div class="flex space-x-6">
            <a
              @click="abrirPrivacidade"
              class="text-gray-400 hover:text-pink-400 text-sm cursor-pointer"
              >Política de Privacidade</a
            >
            <a
              @click="abrirTermos"
              class="text-gray-400 hover:text-pink-400 text-sm cursor-pointer"
              >Termos de Serviço</a
            >
          </div>
        </div>
      </div>
    </div>

    <!-- Uso do componente de modais -->
    <TermosPrivacidadeModais
      :mostrarPrivacidade="showPrivacyModal"
      :mostrarTermos="showTermsModal"
      @atualizar:mostrarPrivacidade="showPrivacyModal = $event"
      @atualizar:mostrarTermos="showTermsModal = $event"
    />
  </footer>
</template>

<script setup>
import { ref } from "vue";
import TermosPrivacidadeModais from "./TermosPrivacidadeModais.vue";

const currentYear = new Date().getFullYear();
const showPrivacyModal = ref(false);
const showTermsModal = ref(false);

const abrirPrivacidade = () => {
  showPrivacyModal.value = true;
};

const abrirTermos = () => {
  showTermsModal.value = true;
};

const scrollToSection = (e, sectionId) => {
  e.preventDefault();
  const section = document.querySelector(sectionId);
  if (section) {
    section.scrollIntoView({ behavior: "smooth" });
  }
};
</script>

<style scoped>
/* Animação suave para o modal */
.fixed {
  transition: opacity 0.2s ease-in-out;
}

.instagram {
  color: rgb(146, 146, 146) !important;
  &:hover {
    color: #e1306c !important;
  }
}
</style>
