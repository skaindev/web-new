<template>
  <component :is="'h' + level" :class="classes" :style="styles">
    <slot />
  </component>
</template>

<script>
export default {
  name: 'VHeading',
  props: {
    level: {
      type: Number,
      default: 1,
      validator: (value) => value > 0 && value < 6,
    },
    color: {
      type: String,
      default: 'primary',
      validator: (value) => ['primary', 'secondary', 'link'].includes(value),
    },
    size: {
      type: String,
      default: null,
    },
    weight: {
      type: Number,
      default: null,
      validator: (value) =>
        [200, 300, 400, 500, 600, 700, 800, 900].includes(value),
    },
    font: {
      type: String,
      default: 'sans',
      validator: (value) => ['sans', 'serif'].includes(value),
    },
    lineHeight: {
      type: String,
      default: null,
    },
    letterSpacing: {
      type: String,
      default: null,
    },
    gradient: {
      type: String,
      default: null,
    },
    transform: {
      type: String,
      default: null,
      validator: (value) =>
        ['uppercase', 'lowercase', 'capitalize'].includes(value),
    },
  },
  data() {
    return {
      classes: {},
      styles: {},
    }
  },
  created() {
    // Classes are coming from assets/css/styles.css
    this.classes['color-' + this.color] = true
    this.classes['font-' + this.font] = true
    if (this.weight) {
      this.styles['font-weight'] = this.weight
    }
    if (this.size?.trim()) {
      this.styles['font-size'] = this.size
    }
    if (this.lineHeight?.trim()) {
      this.styles['line-height'] = this.lineHeight
    }
    if (this.letterSpacing?.trim()) {
      this.styles['letter-spacing'] = this.letterSpacing
    }
    if (this.transform?.trim()) {
      this.styles['text-transform'] = this.transform
    }
    if (this.gradient?.trim()) {
      this.classes.gradient = true
      this.styles.background = this.gradient
    }
  },
}
</script>

<style lang="postcss" scoped>
@import url('./media-query-helper.css');

.gradient {
  background-clip: text !important;
  -webkit-background-clip: text !important;
  -webkit-text-fill-color: transparent !important;
}

h1 {
  font-size: 3rem;
  line-height: 4.875rem;
  font-weight: 700;

  @media (--viewport-medium) {
    font-size: 2.25rem;
    line-height: 2.75rem;
  }
}

h2 {
  font-size: 2.5rem;
  line-height: 3rem;
  font-weight: 600;

  @media (--viewport-medium) {
    font-size: 2.25rem;
    line-height: 2.75rem;
  }
}

h3 {
  font-size: 1.125rem;
  line-height: 1.412rem;
  font-weight: 700;
  letter-spacing: 0.675rem;

  @media (--viewport-medium) {
    font-size: 0.875rem;
    line-height: 1.125rem;
  }
}
</style>
