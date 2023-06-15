<template>
  <div class="bg-white">
    <div class="mx-auto max-w-7xl px-6 py-16 sm:py-24 lg:px-8">
      <h2 class="text-2xl font-bold leading-10 tracking-tight text-gray-900">Peruntas mais frequentes.</h2>
      <p class="mt-6 max-w-2xl text-base leading-7 text-gray-600">Encontre respostas rápidas para suas dúvidas sobre o Quintal de Alegria! Se ainda tiver alguma dúvida ou se precisar de mais informações, não hesite em entrar em contato conosco. Estamos sempre à disposição para ajudar e esclarecer qualquer questão que você possa ter.</p>
      <div class="mt-20">
        <dl class="space-y-16 sm:grid sm:grid-cols-2 sm:gap-x-6 sm:gap-y-16 sm:space-y-0 lg:grid-cols-3 lg:gap-x-10">
          <div v-for="faq in faqs" :key="faq.id">
            <dt class="text-base font-semibold leading-7 text-gray-900">{{ faq.question }}</dt>
            <dd class="mt-2 text-base leading-7 text-gray-600">{{ faq.answer }}</dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>

<script setup>
const faqs = [
  {
    id: 1,
    question: "Quais atividades estão incluídas em uma festa no Quintal de Alegria?",
    answer:
      "Nossas festas incluem uma variedade de atividades lúdicas, como música, cantigas de roda, teatro, fantoches, contação de histórias, arvorismo, e uma visita à nossa brinquedoteca. Todas as atividades são projetadas para serem divertidas, educativas e envolventes para crianças de todas as idades.",
  },
  {
    id: 2,
    question: "Como faço para reservar uma festa no Quintal de Alegria?",
    answer:
      "Para reservar uma festa conosco, entre em contato através do nosso formulário de orçamento, informando os detalhes do seu evento. Nossa equipe entrará em contato para discutir suas necessidades e desejos para a festa.",
  },
  {
    id: 3,
    question: "Qual é a capacidade máxima de convidados no Quintal de Alegria?",
    answer:
      "Nosso espaço é projetado para acomodar um grande número de convidados, porém a capacidade máxima depende do tipo de evento. Entre em contato conosco para discutir detalhes específicos.",
  },
  {
    id: 4,
    question: "Que tipo de comida é servida nas festas?",
    answer:
      "Oferecemos um buffet de alta qualidade com uma variedade de opções de alimentos e bebidas. Podemos adaptar o menu para atender a requisitos dietéticos específicos, basta nos informar com antecedência.",
  },
  {
    id: 5,
    question: "O Quintal de Alegria oferece opções para festas temáticas?",
    answer:
      "Sim, estamos mais do que felizes em acomodar festas temáticas! Basta nos informar o tema no momento da reserva e faremos o possível para criar um ambiente mágico que combina com o tema escolhido.",
  },
  {
    id: 6,
    question: "Existe uma idade mínima ou máxima para as crianças que podem participar das festas?",
    answer:
      "No Quintal de Alegria, acreditamos que diversão não tem idade! Nossas atividades são adequadas para crianças de todas as idades, e garantimos que haverá algo divertido para todos.",
  },
  // More questions...
]
</script>