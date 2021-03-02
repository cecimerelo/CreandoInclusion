<template>
  <div id="app" class="app">
    <v-app>
      <header id="link-logo">
        <div id="container">
          <div class="right" />
          <div id="logo">
            <a :href="baseURL">
              <img
                src="../static/logo.png"
                alt="logo"
                width="18%"
                height="auto"
              >
            </a>
          </div>
          <div>
            <v-row id="links" justify="space-around">
              <v-btn
                v-for="routes in links"
                :key="routes.id"
                :to="`${routes.page}`"
                color="black"
                depressed
                text
                small
                plain
                class="spacing"
                v-bind="attrs"
                v-on="on"
              >
                {{ routes.text }}
              </v-btn>
            </v-row>
          </div>
          <div class="right" />
        </div>
      </header>
    </v-app>
  </div>
</template>

<script>
export default {
  data () {
    return {
      baseURL: undefined,
      links: [
        {
          id: 1,
          text: 'Inicio',
          page: '/Inicio'

        },
        {
          id: 2,
          text: 'Quienes Somos',
          page: '/QuienesSomos'
        },
        {
          id: 3,
          text: 'Servicios',
          page: '/Servicios',
          dropdown: ['Club de Ocio', 'Programas', 'Inserción Laboral', 'Servicio Fisioterapia', 'Servicios Sociosanitarios']
        },
        {
          id: 4,
          text: 'Colabora',
          page: '/Colabora'
        },
        {
          id: 5,
          text: 'Voluntariado',
          page: '/Voluntariado'
        },
        {
          id: 6,
          text: 'Galería',
          page: '/Galeria'
        },
        {
          id: 7,
          text: 'Contacto',
          page: '/Contacto'
        }
      ]
    }
  },

  beforeMount () {
    this.baseURL = window.location.origin
  }
}
</script>

<style>

.spacing {
  margin-right: 20px;
  padding: 0 10px;
}

link-logo {
  display: flex;
  align-items: center;
}

#links div {
  float: left;
}

#logo img {
  z-index: -1;
  width: 250px;
}

#container {
  display: flex;
  justify-content: space-between;
}

#container ul {
  margin-block-start: 1em;
  vertical-align: middle;
  margin: 40px 100px;
  list-style: none;
  line-height: 1;
}

.right {
  margin: 50px;
}

#links {
  padding: 70px 20px 30px;
}

#link-logo a {
  color: #5d5d5d;
  font-size: x-large;
}

#link-logo a:hover {
  color: #000000;
}

#link-logo img {
  Padding: 20px 10px 10px;
}

</style>
