<template>
  <div>
    <header>
      <AppHeader/>
    </header>
    <d-container class="py-4">
      <h1 class="page-heading mb-4">Blog Posts</h1>
      <nuxt/>
    </d-container>
  </div>
</template>

<script>
import AppHeader from '~/components/AppHeader.vue'

export default {
  components: {
    AppHeader
  }
}
</script>
