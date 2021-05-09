<template>
  <div>
    <div class="bottom-page">
      <a :href="baseURL" class="link">Asociación Creando Inclusión </a>
      <div class="info">
        <p>
          © 2019. Todos los derechos reservados. <br>
          C / Anillo Verde Nº 51 C.P. 28032 Madrid, C.I.F. G-88610969 <br>
          Tlf. 623036303 <br>
          info@asociacioncreandoinclusion.org <br>
        </p>
      </div>

      <div class="legal-links">
        <v-row
          align="center"
          justify="space-around"
        >
          <div v-for="link in links" :key="link.id">
            <v-btn
              :to="link.page"
              depressed
              text
              plain
            >
              {{ link.text }}
            </v-btn>
          </div>
        </v-row>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BottomPage',

  data () {
    return {
      baseURL: undefined,
      links: [
        {
          id: 1,
          text: 'Política de cookies',
          page: '/PoliticaDeCookies'
        },
        {
          id: 2,
          text: 'Aviso Legal',
          page: '/AvisoLegal'
        },
        {
          id: 3,
          text: 'Política de privacidad',
          page: '/PoliticaDePrivacidad'
        }
      ]
    }
  },

  beforeMount () {
    this.baseURL = window.location.origin
  }
}
</script>

<style scoped>

a:link {
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

.link {
  color: black;
  font-family: "Roboto", sans-serif;
  font-size: x-large;
}

.bottom-page {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  vertical-align: middle;
  display: table-cell;
}

p {
  font-size: medium;
  background-color: white;
  color: #5d5d5d
}

</style>
