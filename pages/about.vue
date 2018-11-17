<template>
  <div>
    <nuxt-link to="/">TOP</nuxt-link>
    <p>test</p>
  </div>
</template>

<script>
export default {
  layout: 'dark',
  head() {
    return {
      title: 'About',
      meta: [
        { hid: 'description', name: 'description', content: 'Aboutページ' }
      ]
    }
  }
}
</script>

<style lang="scss">
</style>
