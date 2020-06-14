<template>
    <v-app>
        <!-- Menu topo -->
        <v-app-bar
            :clipped-left="clipped"
            fixed
            app
            height="100%"
            color="white"
        >
            <a href="http://triskeleletrificacao.com.br/">
                <v-img
                    src="Imagens/logo.png"
                    contain
                    min-height="90px"
                    min-width="250px"
                    max-height="20%"
                    max-width="20%"
                    position="left"
                />
            </a>

            <v-spacer />

            <v-toolbar-items v-if="$vuetify.breakpoint.smAndUp">
                <v-divider vertical />

                <!-- Botão inicio -->
                <v-btn
                    text
                    to="/"
                    active-class="router-active-class"
                >
                    Inicio
                </v-btn>

                <v-divider vertical />

                <!-- Botão Produtos -->
                <v-btn
                    text
                    to="produtos"
                    active-class="router-active-class"
                >
                    Produtos
                </v-btn>

                <v-divider vertical />

                <!-- Botão Sobre -->
                <v-btn
                    text
                    to="sobre"
                    active-class="router-active-class"
                >
                    Sobre
                </v-btn>

                <v-divider vertical />

                <!-- Botão Contato -->
                <v-btn
                    text
                    to="contato"
                    active-class="router-active-class"
                >
                    Contato
                </v-btn>
                <v-divider vertical />
            </v-toolbar-items>
            <v-app-bar-nav-icon
                v-else
                @click="drawer = true"
            />
        </v-app-bar>

        <v-navigation-drawer
            v-model="drawer"
            right
            mini-variant
            mini-variant-width="150"
            app
        >
            <v-list
                dense
                rounded
                class="py-0"
            >
                <v-list-item class="d-flex justify-center">
                    <v-img src="Imagens/logo.png" />
                </v-list-item>

                <v-divider />

                <v-list-item
                    v-for="({text, to}, i) in options"
                    :key="i"
                    link
                    :to="to"
                    active-class="router-active-class"
                >
                    <v-list-item-content class="text-center">
                        <v-list-item-title>{{ text }}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>

        <!-- Fim menu topo -->

        <v-content>
            <v-container>
                <nuxt /> <!-- ###################### nuxt entra aqui ###################### -->
            </v-container>
        </v-content>

        <!-- Inicio rodapé -->
        <v-footer
            id="footer"
            min-height="27px"
        >
            <v-row
                id="footer"
                no-gutters
            >
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
                    <h4>2020</h4>
                </v-row>
                <v-row
                    align="center"
                    justify="center"
                >
                    <h4>Desenvolvido por </h4>
                    <a href="https://vpuchille.dev">
                        <v-img
                            class="ml-3"
                            src="Imagens\meu-logo.png"
                            max-height="30"
                            max-width="30"
                            to="vpuchille.dev"
                        />
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
            fixed: false,
            options: [
                {
                    to: "/",
                    text: "Início"
                },
                {
                    to: "produtos",
                    text: "Produtos"
                },
                {
                    to: "sobre",
                    text: "Sobre"
                },
                {
                    to: "contato",
                    text: "Contato"
                }
            ],
        };
    },
    created () {

        this.drawer = this.$vuetify.breakpoint.xsOnly ? null : false;

    },
};
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