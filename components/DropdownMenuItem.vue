<template>
  <div id="menu-item" class="links">
    <v-menu
      nudge-left="30"
    >
      <template #activator="{ attrs, on }">
        <v-btn
          color="black"
          depressed
          text
          small
          plain
          class="spacing"
          v-bind="attrs"
          v-on="on"
        >
          {{ text }}
        </v-btn>
      </template>

      <v-list>
        <v-list-item
          v-for="item in dropdownItems"
          :key="item"
          :to="item"
          depressed
          text
          small
          plain
          link
        >
          <div class="dropdown-elements">
            <v-list-item-title> {{ item }} </v-list-item-title>
          </div>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>

<script>
export default {
  name: 'DropdownMenuItem',

  props: {
    page: {
      type: String,
      default: ''
    },
    text: {
      type: String,
      default: ''
    },
    dropdownItems: {
      type: Array,
      default () {
        return []
      }
    }

  }
}
</script>

<style scoped>
.v-btn {
  font-size: 1.2rem;
}

.v-list-item {
  font-family: "Roboto", sans-serif;
  line-height: 1.5;
  text-align: center;
  position: relative;
}

.links {
  padding: 80px 20px 30px;
}

.spacing {
  margin-right: 20px;
  padding: 0 10px;
}

</style>
