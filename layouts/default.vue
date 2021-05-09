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
          <div class="menu">
            <v-row>
              <MenuComponent
                v-for="link in links"
                :key="link.id"
                :link="link"
              />
            </v-row>
          </div>
          <div class="right" />
        </div>
      </header>
      <body>
        <BottomPage />
      </body>
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
          page: '/Inicio',
          simple: true
        },
        {
          id: 2,
          text: 'Quienes Somos',
          page: '/QuienesSomos',
          simple: true
        },
        {
          id: 3,
          text: 'Servicios',
          page: '/Servicios',
          simple: false,
          dropdownItems: ['Servicios', 'Club de Ocio', 'Programas', 'Inserción Laboral', 'Servicio Fisioterapia', 'Servicios Sociosanitarios']
        },
        {
          id: 4,
          text: 'Colabora',
          page: '/Colabora',
          simple: true
        },
        {
          id: 5,
          text: 'Voluntariado',
          page: '/Voluntariado',
          simple: true
        },
        {
          id: 6,
          text: 'Galería',
          page: '/Galeria',
          simple: true
        },
        {
          id: 7,
          text: 'Contacto',
          page: '/Contacto',
          simple: true
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
  margin: 30px;
}

#link-logo a {
  color: #5d5d5d;
}

#link-logo a:hover {
  color: #000000;
}

#link-logo img {
  Padding: 20px 10px 10px;
}

#app {
  background-color:#ffffff;
}

.menu {
  font-size: 0;
}

</style>
