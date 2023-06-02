<template>
  <section class="bg-indigo-700 px-6 py-24 lg:px-8 sm:py-32">
    <ClientOnly>
      <Swiper
    :modules="[SwiperAutoplay]"
    :slides-per-view="1"
    :loop="true"
    :autoplay="{
      delay: 5000,
      disableOnInteraction: true,
      pauseOnMouseEnter: true,
    }"

  >
        <swiper-slide v-for="(testimonial, index) in testimonials" :key="index">
          <figure class="mx-auto max-w-2xl">
            <p class="sr-only">5 out of 5 stars</p>
            <div class="flex gap-x-1 text-yellow-300">
              <StarIcon class="h-5 w-5 flex-none" aria-hidden="true" />
              <StarIcon class="h-5 w-5 flex-none" aria-hidden="true" />
              <StarIcon class="h-5 w-5 flex-none" aria-hidden="true" />
              <StarIcon class="h-5 w-5 flex-none" aria-hidden="true" />
              <StarIcon class="h-5 w-5 flex-none" aria-hidden="true" />
            </div>
            <blockquote class="mt-10 text-xl font-semibold leading-8 tracking-tight text-gray-50 sm:text-2xl sm:leading-9">
              <p>{{ testimonial.quote }}</p>
            </blockquote>
            <figcaption class="mt-10 flex items-center gap-x-6">
              <img class="h-12 w-12 rounded-full bg-gray-50" :src="testimonial.image" alt="">
              <div class="text-sm leading-6">
                <div class="font-semibold text-gray-50">
                  {{ testimonial.name }}
                </div>
                <div class="mt-0.5 text-gray-200">
                  {{ testimonial.position }}
                </div>
              </div>
            </figcaption>
          </figure>
        </swiper-slide>
  
      </swiper>
    </ClientOnly>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/bundle';
import { StarIcon } from '@heroicons/vue/20/solid'

let testimonials = [
  {
    quote: 'Qui dolor enim consectetur do et non ex amet culpa sint in ea non dolore...',
    name: 'Judith Black',
    position: 'CEO of Workcation',
    image: 'https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=1024&h=1024&q=80',
  },
  {
    quote: 'Topzera!!!',
    name: 'Guilherme Diaz',
    position: 'CEO of Workcation',
    image: 'https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=1024&h=1024&q=80',
  },
  {
    quote: 'Estou realmente impressionado com os resultados!',
    name: 'Marina Silva',
    position: 'CTO of Innovatech',
    image: 'https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=1024&h=1024&q=80',
  }
]

defineComponent({
  components: {
    Swiper,
    SwiperSlide,
    StarIcon
  }
})
</script>

