<template>
  <div>
    <v-stack direction="column" gap="1.25rem">
      <v-text
        v-if="title"
        font="serif"
        :weight="700"
        size="1.125rem"
        line-height="1.42rem"
        letter-spacing="0.375rem"
        transform="uppercase"
      >
        <span
          style="margin-right: 0.5rem; font-weight: 900; font-size: 1.2rem"
          class="font-sans"
        >
          |
        </span>
        <span>{{ title }}</span>
      </v-text>
      <v-heading v-if="heading" :level="2" class="heading">
        {{ heading }}
      </v-heading>
      <v-text
        v-if="description"
        color="secondary"
        :weight="400"
        class="description"
      >
        {{ description }}
      </v-text>
    </v-stack>
  </div>
</template>

<script>
export default {
  name: 'AppSectionDescriptor',
  props: {
    title: {
      type: String,
      default: null,
    },
    heading: {
      type: String,
      default: null,
    },
    description: {
      type: String,
      default: null,
    },
  },
}
</script>

<style scoped>
@import url('./lib/media-query-helper.css');

.heading {
  margin-bottom: 1.25rem;
}

.description {
  font-size: 1.375rem;
  line-height: 2rem;
  margin-top: 1.2rem;
  margin-bottom: 1.2rem;;
  color: black;

  @media (--viewport-medium) {
    font-size: 1.125rem;
    line-height: 1.5rem;
  }
}


</style>
