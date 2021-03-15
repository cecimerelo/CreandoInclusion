<template>
  <SimpleMenuItem
    v-if="link.simple"
    :page="link.page"
    :text="link.text"
  />

  <DropdownMenuItem
    v-else
    :page="link.page"
    :text="link.text"
    :dropdown-items="link.dropdownItems"
  />
</template>
<script>

export default {
  name: 'MenuComponent',
  props: {
    link: {
      type: Object,
      default () {
        return {
          id: 0,
          text: '',
          page: '',
          simple: false,
          dropdown: []
        }
      }
    }
  }
}

</script>

<style scoped>

</style>
