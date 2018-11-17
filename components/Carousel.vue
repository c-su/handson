<template>
  <div>
    <button
      type="button"
      name="button"
      @click="plus">プラス</button>
    <transition name="slide">
      <p :key="show">{{ emo[show] }}</p>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0,
      emo: ['😀', '😂', '😎']
    }
  },
  computed: {
    show() {
      return this.num % 3
    }
  },
  methods: {
    plus() {
      this.num++
    }
  }
}
</script>

<style>
.slide-enter-active,
.slide-leave-active {
  transition: transform 0.5s;
}
.slide-enter {
  transform: translateX(50px);
}
.slide-leave-active {
  transform: translateX(-50px);
}

p {
  position: absolute;
  margin: 0;
  font-size: 3em;
}
</style>
