<template>
  <div id="menu-item" class="links">
    <v-btn
      color="black"
      :to="page"
      depressed
      text
      small
      plain
      class="spacing"
    >
      {{ text }}
    </v-btn>
  </div>
</template>

<script>
export default {
  name: 'SimpleMenuItem',
  props: {
    page: {
      type: String,
      default: ''
    },
    text: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped>

.v-btn {
  font-size: 1.2rem;
}

.links {
  padding: 80px 20px 20px;
}

.spacing {
  margin-right: 20px;
  padding: 0 10px;
}

</style>
