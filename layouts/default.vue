<template>
  <v-app>
    <!-- ################ Menu topo ############### -->
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      height=90px
      color=white

    >
      <a href="http://triskeleletrificacao.com.br/">
        <v-img
          src="Imagens/logo.png"
          contain
          max-height=90px
          max-width=250px
          position="left">
        </v-img>
      </a>

      <v-spacer />

      <v-toolbar-items>

        <v-divider vertical></v-divider>

        <!-- Botão inicio -->
        <v-btn
          text
          to="/"
          active-class="router-active-class"
        >
          Inicio
        </v-btn>

        <v-divider vertical></v-divider>

        <!-- Botão Produtos -->
        <v-btn
          text
          to="produtos"
          active-class="router-active-class"
        >
          Produtos
        </v-btn>

        <v-divider vertical></v-divider>

        <!-- Botão Sobre -->
        <v-btn
          text
          to="sobre"
          active-class="router-active-class"
        >
          Sobre
        </v-btn>

        <v-divider vertical></v-divider>

        <!-- Botão Contato -->
        <v-btn
          text
          to="contato"
          active-class="router-active-class"
        >
          Contato
        </v-btn>
        <v-divider vertical></v-divider>

      </v-toolbar-items>
    </v-app-bar>
    <!-- Fim menu topo -->

    <v-content>
      <v-container>
        <nuxt /> <!-- ###################### nuxt entra aqui ###################### -->
      </v-container>
    </v-content>

    <!-- Inicio rodapé -->
    <v-footer
      id="footer"
      min-height=27px
    >
      <v-row no-gutters id="footer">
        <v-row
          align="center"
          justify="center"
        >
          <v-col
            align="center"
            justify="end"
          >
            <a href="https://www.linkedin.com/in/triskel-eletrifica%C3%A7%C3%A3o-e-automa%C3%A7%C3%A3o-518a721a6/">
              <v-icon
                id="icon_footer"
                size="40px"
              >
                mdi mdi-linkedin
              </v-icon>
            </a>

            <a href="https://www.instagram.com/triskeleletrificacao/">
              <v-icon
                id="icon_footer"
                size="40px"
              >
                mdi mdi-instagram
              </v-icon>
            </a>
          </v-col>
        </v-row>
        <v-row
          align="center"
          justify="center"
        >
          <v-icon> mdi mdi-copyright</v-icon>
          <h3>2020</h3>
        </v-row>
        <v-row
          align="center"
          justify="center"
        >
          <h3>Developed by .</h3>
          <a href="https://vpuchille.dev">
            <v-img
              src="Imagens\meu-logo.png"
              max-height="30"
              max-width="30"
              to="vpuchille.dev"
            >
            </v-img>
          </a>
        </v-row>
      </v-row>
    </v-footer>
    <!-- Fim rodapé -->
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
    }
  }
}
</script>

<style scoped>
  #footer{
    background-color: #f2f2f2ff;
  }

  #pag_actual{
    background-color: #a91d21ff;
  }

  #icon_footer{
    color:#a91d21ff;
  }

  .router-active-class{
    background-color: #a91d21ff;
    color: white;
  }

</style>