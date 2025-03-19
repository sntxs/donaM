<template>
  <!-- Modal de Política de Privacidade -->
  <div v-if="showPrivacyModal" class="fixed inset-0 z-50 flex items-center justify-center px-4 sm:px-0">
    <div class="fixed inset-0 bg-black opacity-50" @click="fecharPrivacidade"></div>
    <div class="relative bg-white text-gray-800 rounded-lg shadow-xl max-w-2xl w-full max-h-[90vh] overflow-y-auto">
      <div class="sticky top-0 bg-white px-6 py-4 border-b border-gray-200 flex justify-between items-center">
        <h2 class="text-xl font-bold text-pink-600">Política de Privacidade</h2>
        <button @click="fecharPrivacidade" class="text-gray-500 hover:text-gray-800">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
      <div class="px-6 py-4">
        <div class="space-y-4">
          <h3 class="text-lg font-semibold">1. Informações Coletadas</h3>
          <p>A Dona M Confeitaria valoriza a sua privacidade e está comprometida em proteger seus dados pessoais. Coletamos as seguintes informações:</p>
          <ul class="list-disc pl-5 space-y-1">
            <li>Informações de contato (nome, telefone, e-mail)</li>
            <li>Endereço para entrega de produtos</li>
            <li>Preferências de produtos e histórico de compras</li>
            <li>Informações sobre sua interação com nosso site e redes sociais</li>
          </ul>
          
          <h3 class="text-lg font-semibold mt-6">2. Uso das Informações</h3>
          <p>Utilizamos suas informações para:</p>
          <ul class="list-disc pl-5 space-y-1">
            <li>Processar e entregar seus pedidos</li>
            <li>Melhorar nossos produtos e serviços</li>
            <li>Comunicar promoções e novos produtos</li>
            <li>Responder às suas dúvidas e solicitações</li>
          </ul>
          
          <h3 class="text-lg font-semibold mt-6">3. Compartilhamento de Dados</h3>
          <p>Não vendemos ou alugamos suas informações pessoais a terceiros. Podemos compartilhar informações com:</p>
          <ul class="list-disc pl-5 space-y-1">
            <li>Parceiros de entrega para realizar a entrega de produtos</li>
            <li>Processadores de pagamento para completar transações</li>
            <li>Autoridades quando exigido por lei</li>
          </ul>
          
          <h3 class="text-lg font-semibold mt-6">4. Cookies e Tecnologias Semelhantes</h3>
          <p>Utilizamos cookies para melhorar sua experiência em nosso site, analisar o tráfego e personalizar conteúdo. Você pode controlar cookies através das configurações do seu navegador.</p>
          
          <h3 class="text-lg font-semibold mt-6">5. Seus Direitos</h3>
          <p>Você tem o direito de:</p>
          <ul class="list-disc pl-5 space-y-1">
            <li>Acessar, corrigir ou excluir seus dados pessoais</li>
            <li>Retirar seu consentimento a qualquer momento</li>
            <li>Solicitar restrição do processamento de seus dados</li>
            <li>Receber seus dados em formato estruturado</li>
          </ul>
          
          <h3 class="text-lg font-semibold mt-6">6. Segurança de Dados</h3>
          <p>Implementamos medidas de segurança técnicas e organizacionais para proteger seus dados pessoais contra acesso não autorizado, perda ou alteração.</p>
          
          <h3 class="text-lg font-semibold mt-6">7. Contato</h3>
          <p>Se você tiver dúvidas sobre nossa Política de Privacidade, entre em contato conosco pelo WhatsApp (18) 98145-3272.</p>
          
          <p class="text-sm text-gray-500 mt-6">Última atualização: {{ dataAtual }}</p>
        </div>
      </div>
    </div>
  </div>
  
  <!-- Modal de Termos de Serviço -->
  <div v-if="showTermsModal" class="fixed inset-0 z-50 flex items-center justify-center px-4 sm:px-0">
    <div class="fixed inset-0 bg-black opacity-50" @click="fecharTermos"></div>
    <div class="relative bg-white text-gray-800 rounded-lg shadow-xl max-w-2xl w-full max-h-[90vh] overflow-y-auto">
      <div class="sticky top-0 bg-white px-6 py-4 border-b border-gray-200 flex justify-between items-center">
        <h2 class="text-xl font-bold text-pink-600">Termos de Serviço</h2>
        <button @click="fecharTermos" class="text-gray-500 hover:text-gray-800">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
      <div class="px-6 py-4">
        <div class="space-y-4">
          <h3 class="text-lg font-semibold">1. Aceitação dos Termos</h3>
          <p>Ao acessar e utilizar os serviços da Dona M Confeitaria, você concorda com estes Termos de Serviço. Se você não concordar com qualquer parte destes termos, não deverá utilizar nossos serviços.</p>
          
          <h3 class="text-lg font-semibold mt-6">2. Produtos e Serviços</h3>
          <p>A Dona M Confeitaria oferece produtos de confeitaria artesanal para diversas ocasiões. Todos os produtos são preparados com ingredientes selecionados e seguindo as melhores práticas de higiene e segurança alimentar.</p>
          <p class="mt-2">As imagens dos produtos são meramente ilustrativas e podem apresentar pequenas variações em relação ao produto final, devido à natureza artesanal de nossa produção.</p>
          
          <h3 class="text-lg font-semibold mt-6">3. Pedidos e Pagamentos</h3>
          <p>Os pedidos devem ser realizados com antecedência mínima de 48 horas, sujeitos à disponibilidade. Para eventos especiais, recomendamos fazer o pedido com maior antecedência.</p>
          <p class="mt-2">Aceitamos as seguintes formas de pagamento:</p>
          <ul class="list-disc pl-5 space-y-1">
            <li>Pagamento via PIX</li>
            <li>Transferência bancária</li>
            <li>Dinheiro na entrega</li>
          </ul>
          <p class="mt-2">Um sinal de 50% do valor é necessário para confirmar a reserva do pedido.</p>
          
          <h3 class="text-lg font-semibold mt-6">4. Cancelamentos e Alterações</h3>
          <p>Cancelamentos ou alterações de pedidos devem ser solicitados com antecedência mínima de 24 horas da data de entrega. Cancelamentos com menos de 24 horas não são passíveis de reembolso do sinal.</p>
          
          <h3 class="text-lg font-semibold mt-6">5. Entregas</h3>
          <p>Realizamos entregas em toda a região mediante taxa adicional, calculada conforme a distância. O cliente é responsável por fornecer o endereço correto e completo.</p>
          <p class="mt-2">Em caso de ausência no momento da entrega, tentaremos contato por telefone. Após 30 minutos sem resposta, retornaremos com o produto e será necessário agendar nova entrega.</p>
          
          <h3 class="text-lg font-semibold mt-6">6. Alergias e Restrições Alimentares</h3>
          <p>É responsabilidade do cliente informar sobre alergias ou restrições alimentares no momento do pedido. Embora tomemos precauções, nossos produtos são preparados em ambiente que manipula diversos ingredientes alérgenos.</p>
          
          <h3 class="text-lg font-semibold mt-6">7. Propriedade Intelectual</h3>
          <p>Todo o conteúdo deste site, incluindo imagens, textos, logotipos e design, é propriedade exclusiva da Dona M Confeitaria e está protegido por leis de direitos autorais.</p>
          
          <h3 class="text-lg font-semibold mt-6">8. Alterações nos Termos</h3>
          <p>Reservamo-nos o direito de modificar estes termos a qualquer momento. As alterações entram em vigor imediatamente após sua publicação no site.</p>
          
          <h3 class="text-lg font-semibold mt-6">9. Contato</h3>
          <p>Para dúvidas ou esclarecimentos sobre estes Termos de Serviço, entre em contato pelo WhatsApp (18) 98145-3272.</p>
          
          <p class="text-sm text-gray-500 mt-6">Última atualização: {{ dataAtual }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed, watch } from 'vue';

// Props para controlar a exibição dos modais
const props = defineProps({
  mostrarPrivacidade: {
    type: Boolean,
    default: false
  },
  mostrarTermos: {
    type: Boolean,
    default: false
  }
});

// Emits para comunicar com o componente pai
const emit = defineEmits(['atualizar:mostrarPrivacidade', 'atualizar:mostrarTermos']);

// Refs reativas para controlar internamente o estado dos modais
const showPrivacyModal = ref(props.mostrarPrivacidade);
const showTermsModal = ref(props.mostrarTermos);

// Observar mudanças nas props
watch(() => props.mostrarPrivacidade, (novo) => {
  showPrivacyModal.value = novo;
  if (novo) document.body.style.overflow = 'hidden';
  else document.body.style.overflow = '';
});

watch(() => props.mostrarTermos, (novo) => {
  showTermsModal.value = novo;
  if (novo) document.body.style.overflow = 'hidden';
  else document.body.style.overflow = '';
});

// Métodos para fechar os modais
const fecharPrivacidade = () => {
  emit('atualizar:mostrarPrivacidade', false);
  document.body.style.overflow = '';
};

const fecharTermos = () => {
  emit('atualizar:mostrarTermos', false);
  document.body.style.overflow = '';
};

// Data formatada em português
const dataAtual = computed(() => {
  return new Date().toLocaleDateString('pt-BR');
});
</script>

<style scoped>
/* Animação suave para o modal */
.fixed {
  transition: opacity 0.2s ease-in-out;
}
</style> 