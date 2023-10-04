<script setup lang="ts">
const props = defineProps({
  direction: {
    default: 'top',
  }
})
</script>

<template>
<div v-if="$slidev.nav.clicks >= 1" v-motion
    :initial="{
      opacity: 0,
      x: 20,
    }"
    :enter="{
      opacity: 1,
      x: 0,
      transition: {
        type: 'spring',
        stiffness: '100',
        delay: 300,
      },
    }"
    class="absolute max-w-16rem right-1/7 top-1/5 z-1"
    :class="{'right-1/7' : props.direction === 'right', 'left-1/7' : props.direction === 'left'}">
  <LightOrDark>
    <template #dark>
      <svg width="255" height="186" viewBox="0 0 255 186" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path v-if="props.direction === 'right'" d="M45 140.5L41 138L0 160.5L54 157L45 140.5Z" stroke="black" stroke-width="2" fill="#FFF"/>
        <path v-if="props.direction === 'top'" d="M72.1502 144.848L76.8671 144.816L99.9819 185.473L55.8352 154.179L72.1502 144.848Z" stroke="black" stroke-width="2" fill="#FFF"/>
        <path v-if="props.direction === 'left'" d="M210 140.5L214 138L255 160.5L201 157L210 140.5Z" stroke="black" stroke-width="2" fill="#FFF"/>
        <path d="M113.34 0L23.63 30.59L8 99.23L42.49 157L202.37 157.34L254.71 94.47L223.61 23.11L113.34 0Z" stroke="black" stroke-width="2" stroke-dasharray="1150" :stroke-dashoffset="direction === 'right' ? '58rem' : '118.5rem'" fill="#FFF"/>
      </svg>
    </template>
    <template #light>
      <svg width="255" height="186" viewBox="0 0 255 186" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path v-if="props.direction === 'right'" d="M45 140.5L41 138L0 160.5L54 157L45 140.5Z" stroke="#56ac8a" stroke-width="2" fill="#FFF"/>
        <path v-if="props.direction === 'top'" d="M72.1502 144.848L76.8671 144.816L99.9819 185.473L55.8352 154.179L72.1502 144.848Z" stroke="#56ac8a" stroke-width="2" fill="#FFF"/>
        <path v-if="props.direction === 'left'" d="M210 140.5L214 138L255 160.5L201 157L210 140.5Z" stroke="#56ac8a" stroke-width="2" fill="#FFF"/>
        <path d="M113.34 0L23.63 30.59L8 99.23L42.49 157L202.37 157.34L254.71 94.47L223.61 23.11L113.34 0Z" stroke="#56ac8a" stroke-width="2" stroke-dasharray="1150" :stroke-dashoffset="direction === 'right' ? '58rem' : '118.5rem'" fill="#FFF"/>
      </svg>
    </template>
  </LightOrDark>

  <div class="absolute top-2/9 h-5/10 w-full flex place-content-center place-items-center text-black px-6 overflow-hidden">
    <slot></slot>
  </div>
</div>
</template>
