<template>
  <v-app>
    <!-- ################ Menu topo ############### -->
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      height=100px
      color=white

    >
      <v-img
        src="Imagens/logo.png"
        contain
        max-height=100px
        max-width=250px
        position="left">
      </v-img>

      <v-divider dark ></v-divider>

      <v-toolbar-title v-text="title" />

      <v-toolbar-items>

        <v-divider vertical></v-divider>

        <!-- Botão inicio -->
        <v-btn text>
          Inicio
        </v-btn>

        <v-divider vertical></v-divider>

        <!-- Botão Produtos -->
        <v-btn text>
          Produtos
        </v-btn>

        <v-divider vertical></v-divider>

        <!-- Botão Sobre -->
        <v-btn text>
          Sobre
        </v-btn>

        <v-divider vertical></v-divider>

        <!-- Botão Contato -->
        <v-btn text>
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
    <v-footer id="footer">
      <v-img
        src="Imagens/logo.png"
        contain
        max-height=100px
        max-width=250px
        position="left">
      </v-img>

      <v-spacer />

      <v-toolbar-items>

          <v-divider vertical></v-divider>

          <!-- Botão inicio -->
          <v-btn text>
            Inicio
          </v-btn>

          <v-divider vertical></v-divider>

          <!-- Botão Produtos -->
          <v-btn text>
            Produtos
          </v-btn>

          <v-divider vertical></v-divider>

          <!-- Botão Sobre -->
          <v-btn text>
            Sobre
          </v-btn>

          <v-divider vertical></v-divider>

          <!-- Botão Contato -->
          <v-btn text>
            Contato
          </v-btn>
          <v-divider vertical></v-divider>
        </v-toolbar-items>

    </v-footer>
    <v-footer id="footer">
      <v-divider />
    </v-footer >
    <v-footer
      id="footer"
      min-height=27px
    >
      <v-container id="flooter">
        <v-row no-gutters>
          <v-col>
            <v-img
              src="Imagens\endereco.png"
              max-height="102px"
              max-width="196px"
            >
            </v-img>
          </v-col>
          <v-col>
            <v-img
              src="Imagens\contato.png"
              max-height="84px"
              max-width="275px"
            >
            </v-img>
          </v-col>
          <v-col>
            <v-row justify="center">
              <v-col>
                <v-img
                  src="Imagens\Linkedin.png"
                  max-height="41px"
                  max-width="41px"
                >
                </v-img>
              </v-col>
              <v-col>
                <v-img
                  src="Imagens\Instagram.png"
                  max-height="41px"
                  max-width="41px"
                >
                </v-img>
              </v-col>
            </v-row>
            <v-row justify="center">
              <h3>Developed by .</h3>
              <v-img
                src="Imagens\meu-logo.png"
                max-height="30"
                max-width="30"
              >
              </v-img>
            </v-row>
          </v-col>
        </v-row>
      </v-container>

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


</style>