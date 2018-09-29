<template>
  <d-navbar toggleable="md" type="dark" theme="primary" v-if="ready">
    <d-navbar-toggle target="nav-collapse"></d-navbar-toggle>
    <d-navbar-brand>
        <h6 class="text-white my-auto mr-4">Shards Vue</h6>
    </d-navbar-brand>

    <d-collapse is-nav id="nav-collapse">
      <d-navbar-nav >
          <d-nav-item to="/about">About</d-nav-item>
          <d-nav-item to="/projects">Projects</d-nav-item>
          <d-nav-item to="/blog">Blog</d-nav-item>
          <d-dropdown text="Blog Categories" is-nav>
              <d-dropdown-item>Vue.js</d-dropdown-item>
              <d-dropdown-item>Nuxt.js</d-dropdown-item>
              <d-dropdown-item>Something else here</d-dropdown-item>
              <d-dropdown-divider />
              <d-dropdown-item>Separated link</d-dropdown-item>
          </d-dropdown>
      </d-navbar-nav>

      <d-navbar-nav class="ml-auto">
          <d-input-group seamless>
              <d-input-group-text slot="prepend">
                  <!-- <fa :icon="['fas', 'search']" /> -->
              </d-input-group-text>
              <d-input size="sm" placeholder="Search..."/>
          </d-input-group>
      </d-navbar-nav>
    </d-collapse>
  </d-navbar>
</template>

<script>
export default {
  name: 'AppHeader',
  data: () => ({
    ready: false
  }),
  mounted() {
    this.$nextTick(() => {
      this.ready = true
    })
  }
}
</script>

<style lang="css">
.nav-link {
  color: white !important;
}
</style>
