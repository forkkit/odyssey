<template>
   <RouterLink
    v-if="isInternal"
    class="nav-link"
    :to="link"
  >
    {{ item.title }}
  </RouterLink>
  <a
    v-else
    :href="link"
    class="nav-link external"
    :target="target"
    :rel="rel"
  >
    {{ item.title }}
  </a>
</template>

<script>
import { isExternal, isMailto, isTel, ensureExt } from '../utils'

export default {
  name: 'SidebarLink',
  props: {
    item: {
      required: true
    }
  },
  computed: {
    link () {
      return ensureExt(this.item.link)
    },
    exact () {
      if (this.$site.locales) {
        return Object.keys(this.$site.locales).some(rootLink => rootLink === this.link)
      }
      return this.link === '/'
    },
    isNonHttpURI () {
      return isMailto(this.link) || isTel(this.link)
    },
    isBlankTarget () {
      return this.target === '_blank'
    },
    isInternal () {
      return !isExternal(this.link) && !this.isBlankTarget
    },
    target () {
      if (this.isNonHttpURI) {
        return null
      }
      if (this.item.target) {
        return this.item.target
      }
      return isExternal(this.link) ? '_blank' : ''
    },
    rel () {
      if (this.isNonHttpURI) {
        return null
      }
      if (this.item.rel) {
        return this.item.rel
      }
      return this.isBlankTarget ? 'noopener noreferrer' : ''
    }
  }
}
</script>
