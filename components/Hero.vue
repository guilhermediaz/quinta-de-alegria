<script>
export default {
  data() {
    return {
      images: [
        'http://quintaldealegria.com.br/wp/wp-content/uploads/2018/05/25299420_1844628582244851_383331152178552603_n.jpg',
        'http://quintaldealegria.com.br/wp/wp-content/uploads/2018/05/25299213_1844627138911662_7560520250905591908_n.jpg',
        'http://quintaldealegria.com.br/wp/wp-content/uploads/2018/05/25299167_1844630405578002_62103332903061137_n.jpg',
        'http://quintaldealegria.com.br/wp/wp-content/uploads/2018/05/28872791_1949532325087809_4329065563144098709_n.jpg',
        // adicione mais links de imagens aqui...
      ],
      currentImage: '',
    }
  },
  mounted() {
    this.randomizeImage()
  },
  methods: {
    randomizeImage() {
      this.currentImage = this.images[Math.floor(Math.random() * this.images.length)]
    },
  },
}
</script>

<template>
  <div class="relative bg-white">
    <div class="mx-auto max-w-7xl lg:grid lg:grid-cols-12 lg:gap-x-8 lg:px-8">
      <div class="px-6 pb-24 pt-10 lg:col-span-7 xl:col-span-6 lg:px-0 lg:pb-56 lg:pt-48 sm:pb-32">
        <div class="mx-auto max-w-2xl lg:mx-0">
          <img class="h-11" src="https://tailwindui.com/img/logos/mark.svg?color=indigo&amp;shade=600" alt="Your Company">
          <div class="hidden lg:mt-16 sm:mt-32 sm:flex">
            <div class="relative rounded-full px-3 py-1 text-sm leading-6 text-gray-500 ring-1 ring-gray-900/10 hover:ring-gray-900/20">
              Anim aute id magna aliqua ad ad non deserunt sunt. <a href="#" class="whitespace-nowrap font-semibold text-indigo-600"><span class="absolute inset-0" aria-hidden="true" />Read more <span aria-hidden="true">&rarr;</span></a>
            </div>
          </div>
          <h1 class="mt-24 text-4xl font-bold tracking-tight text-gray-900 sm:mt-10 sm:text-5xl">
            Diferente de tudo que você já viu. Igual a tudo que você lembrava.
          </h1>
          <p class="mt-6 text-lg leading-8 text-gray-600">
            Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui lorem cupidatat commodo. Elit sunt amet fugiat veniam occaecat fugiat aliqua.
          </p>
          <div class="mt-10 flex items-center gap-x-6">
            <a href="#" class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline-2 focus-visible:outline-indigo-600 focus-visible:outline-offset-2 focus-visible:outline">Get started</a>
            <a href="#" class="text-sm font-semibold leading-6 text-gray-900">Learn more <span aria-hidden="true">→</span></a>
          </div>
        </div>
      </div>
      <div class="relative xl:absolute xl:inset-0 xl:left-1/2 lg:col-span-5 xl:mr-0 lg:-mr-8">
        <img
          class="aspect-[3/2] w-full bg-gray-50 object-cover lg:absolute lg:inset-0 lg:aspect-auto lg:h-full"
          :src="currentImage"
          alt=""
        >
      </div>
    </div>
  </div>
</template>
