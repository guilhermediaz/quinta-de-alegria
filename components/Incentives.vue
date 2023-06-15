<template>
  <div class="bg-white">
    <h2 class="sr-only">Our perks</h2>
    <div class="mx-auto max-w-7xl py-24 sm:px-2 sm:py-32 lg:px-4">
      <div class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-12 px-4 lg:max-w-none lg:grid-cols-2 lg:gap-y-16">
        <div v-for="perk in perks" :key="perk.name" class="sm:flex">
          <div class="sm:flex-shrink-0">
            <div class="flow-root">
              <Icon :class="`h-24 w-28 ${perk.color}`" :name="perk.imageSrc" />
            </div>
          </div>
          <div class="mt-3 sm:ml-3 sm:mt-0">
            <h3 class="text-lg font-bold text-gray-900">{{ perk.name }}</h3>
            <p class="mt-2 text-base text-gray-500">{{ perk.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const perks = [
  {
    name: 'Arvorismo',
    imageSrc: 'zondicons:location-park',
    color: 'text-green-500',
    description: "Experimente a emoção do arvorismo! Nossa atividade de arvorismo é segura, divertida e perfeita para liberar a energia das crianças.",
  },
  {
    name: 'Atividades Lúdicas',
    imageSrc: 'ic:baseline-diversity-3',
    color: 'text-blue-500',
    description: "Redescubra a alegria das brincadeiras clássicas em mais de 600 metros quadrados repletos de música, teatro, fantoches, contação de histórias e uma fantástica brinquedoteca.",
  },
  {
    name: 'Experiência Personalizada',
    imageSrc: 'mdi:puzzle',
    color: 'text-red-500',
    description: "Cada festa é única e personalizada de acordo com os desejos do aniversariante. Compartilhe seus gostos e preferências e deixe nossa equipe planejar um evento inesquecível.",
  },
  {
    name: 'Conexão com o Passado',
    imageSrc: 'bi:watch',
    color: 'text-orange-500',
    description: "Vivencie uma conexão profunda com o passado através de nossas atividades que celebram a cultura popular e as brincadeiras tradicionais da nossa infância.",
  },
]

</script>