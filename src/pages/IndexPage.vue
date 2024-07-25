<template>
  <q-page>
    <q-carousel
      :ref="carousel"
      v-model="slide"
      :autoplay="autoplay"
      :fullscreen="true"
      transition-prev="flip-down"
      transition-next="flip-up"
      animated
      infinite
      vertical
      swipeable
      padding
    >
      <q-carousel-slide
        v-for="(n, key) in 21"
        :key="key"
        :name="n"
        :img-src="`boats/${n}.jpg`"
      />
    </q-carousel>
  </q-page>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const carousel = ref();
const slide = ref(1);
const autoplay = ref(true);
</script>

<style></style>
