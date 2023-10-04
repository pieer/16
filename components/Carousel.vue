<script setup lang="ts">
  import { VueperSlides, VueperSlide } from 'vueperslides'
  import 'vueperslides/dist/vueperslides.css'

  const slides =  [
    {
      title: 'vue mastery',
      image: 'vue-mastery.jpg',
      link: 'https://www.vuemastery.com/'
    }, {
      title: 'advaya',
      image: 'advaya.png',
      link: 'https://advaya.life/'
    }, {
      title: 'nanda hobbs',
      image: 'nanda-hobbs.jpg',
      link: 'https://nandahobbs.com/'
    }, {
      title: 'taxonomy of design',
      image: 'taxonomy-of-design.jpg',
      link: 'http://taxonomyofdesign.com/'
    }, {
      title: 'pollen',
      image: 'pollen.jpg',
      link: 'https://www.pollen.com.au/'
    }, {
      title: 'group income',
      image: 'group-income.jpg',
      link: 'https://okturtles.github.io/groupincome.org/'
    }, {
      title: 'i touch myself',
      image: 'i-touch-myself.jpg',
      link: 'https://itouchmyself.org/'
    }, {
      title: 'quay',
      image: 'quay.jpg',
      link: 'https://www.pollen.com.au/'
    }, {
      title: 'upwire',
      image: 'upwire.jpg',
      link: 'https://www.upwire.com/'
    }
  ]


</script>

<template>
<vueper-slides
  class="no-shadow pt-3"
  :bullets="false"
  :transition-speed="500"
  :dragging-distance="200"
  :breakpoints="{ 800: { visibleSlides: 1, slideMultiple: 1 } }"
  autoplay="true"
  fade="true"
  :infinite="true"
  :pause-on-hover="false"
>
  <vueper-slide
    class="bg-contain bg-no-repeat"
    v-for="(slide, i) in slides"
    :key="i"
    :image="`/websites/${slide.image}`"
    :link='slide.link'
    open-in-new
  />
</vueper-slides>
</template>
