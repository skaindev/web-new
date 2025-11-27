<template>
  <img
    :class="{ responsive }"
    :height="dimension[1] ? dimension[1] : ''"
    :src="resolvedPath"
    :style="styles"
    :width="dimension[0] ? dimension[0] : ''"
    @click.stop="(ev) => $emit('click', ev)"
    @mouseenter="(ev) => $emit('mouseenter', ev)"
    @mouseleave="(ev) => $emit('mouseleave', ev)"
  />
</template>

<script>
export default {
  name: 'VImage',
  props: {
    path: {
      type: String,
      required: true,
    },
    responsive: {
      type: Boolean,
    },
    width: {
      type: String,
      default: null,
    },
    height: {
      type: String,
      default: 'auto',
    },
    maxWidth: {
      type: String,
      default: null,
    },
    minWidth: {
      type: String,
      default: null,
    },
    dimension: {
      type: Array,
      default() {
        return []
      },
    },
  },
  data() {
    return {
      styles: {},
    }
  },
  computed: {
    resolvedPath() {
      return require(`~/assets/${this.path}`)
    },
  },
  created() {
    this.styles.height = this.height
    if (this.width) {
      this.styles.width = this.width
    }
    if (this.maxWidth) {
      this.styles['max-width'] = this.maxWidth
    }
    if (this.minWidth) {
      this.styles['min-width'] = this.minWidth
    }
  },
}
</script>

<style lang="postcss" scoped>
.responsive {
  width: 100%;
  height: auto;
}
</style>
