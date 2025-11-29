<template>
  <div class="input-group">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'VInputGroup',
}
</script>

<style lang="postcss" scoped>
.input-group {
  display: flex;
}
.input-group *:not(:first-child) {
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}
.input-group *:not(:last-child) {
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
</style>
