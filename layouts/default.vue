<template>
  <div id="app">
    <v-app>
      <v-toolbar
        flat
        prominent
      >
        <a id="logo" :href="baseURL">
          <img
            src="../static/logo.jpg"
            alt="logo"
            width="18%"
            height="auto"
          >
        </a>
      </v-toolbar>
    </v-app>
  </div>
</template>

<script>
export default {
  data () {
    return {
      baseURL: undefined
    }
  },

  beforeMount () {
    this.baseURL = window.location.origin
  }
}
</script>
