<template>
  <b-card-img v-if="!$fetchState.pending" v-bind="props" />
</template>

<script>
import DruxtFieldResponsiveImage from './DruxtFieldResponsiveImage.vue'

export default {
  name: 'DruxtFieldResponsiveImageFieldMediaImage',

  extends: DruxtFieldResponsiveImage,

  computed: {
    props() {
      return {
        src: this.entities[0].attributes.uri.url,
        top: true,
      }
    },
  },
}
</script>
