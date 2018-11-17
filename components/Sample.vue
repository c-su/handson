<template lang="html">
  <div class="sample">
    <h1>{{ title }}</h1>
    <div>
      <button
        type="button"
        name="button"
        @click="plus">click times: {{ num }}
      </button>
    </div>
    <div :class="['hide', { seven: num === 7}]">
      click 7 times
    </div>
    Hello, I'm {{ name }} {{ reverseName }}
    <transition name="fade">
      <slot/>
    </transition>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Default Title'
    }
  },
  data() {
    return {
      name: 'c-su',
      num: 0
    }
  },
  computed: {
    reverseName() {
      return this.name
        .split('')
        .reverse()
        .join('')
    }
  },
  mounted() {
    console.log('mounted')
  },
  methods: {
    plus() {
      this.num++
    }
  }
}
</script>

<style lang="scss" scoped>
.hide {
  display: none;
  &.seven {
    display: block;
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
