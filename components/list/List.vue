<template>
  <ul
    :class="classes"
    class="mdc-list">
    <slot />
  </ul>
</template>

<script>
import { baseComponentMixin, themeClassMixin } from '../base'

export default {
  mixins: [baseComponentMixin, themeClassMixin],
  props: {
    avatar: {
      type: Boolean,
      default: false
    },
    dense: {
      type: Boolean,
      default: false
    },
    twoLine: {
      type: Boolean,
      default: false
    },
    nonInteractive: {
      type: Boolean,
      default: false
    }
  },
  computed: {
    classes () {
      return {
        'mdc-list--dense': this.dense,
        'mdc-list--two-line': this.twoLine,
        'mdc-list--avatar-list': this.avatar,
        'mdc-list--non-interactive': this.nonInteractive
      }
    }
  }
}
</script>
