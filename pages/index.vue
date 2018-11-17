<template>
  <div>
    <nuxt-link to="/about">About</nuxt-link>
    <div>
      <sample title="うえい">test</sample>
      <carousel/>
    </div>
  </div>
</template>

<script>
import Sample from '~/components/Sample.vue'
import Carousel from '~/components/Carousel.vue'

export default {
  components: {
    Sample,
    Carousel
  }
}
</script>

<style>
</style>
