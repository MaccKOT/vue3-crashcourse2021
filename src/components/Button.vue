<template>
  <button
    :style="{ background: color }"
    class="btn"
    @click="onClick()"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: String,
    color: String,
  },
  emits: ['btn-click'],
  methods: {
    onClick() {
      this.$emit('btn-click')
    },
  },
}
</script>