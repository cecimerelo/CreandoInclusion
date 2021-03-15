<template>
  <div id="menu-item" class="links">
    <v-btn
      color="black"
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
  name: 'MenuComponent',
  props: {
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
  padding: 80px 20px 30px;
}

.spacing {
  margin-right: 20px;
  padding: 0 10px;
}

</style>
