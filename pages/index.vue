<template>
    <div>
        <!-- Rooter Element -->
        <!-- Carrossel -->

        <v-carousel
            id="carrossel"
            cycle
            height="500px"
            hide-delimiters
            show-arrows-on-hover
        >
            <v-carousel-item
                v-for="(slide, i) in slides"
                :key="i"
                :src="slide.img"
            >
                <v-container
                    class="pa-10 ma-10 pl-12 ml-12"
                >
                    <v-row
                        id="slide-box"
                    >
                        <div
                            id="slide-text-area"
                            class="pa-4"
                        >
                            <h3 id="slide-text-welcome">
                                Bem vindo a Triskel!
                            </h3>
                            <h2 id="slide-text-title">
                                {{ slide.title }}
                            </h2>
                            <p id="slide-text-text">
                                Paineis elétricos de qualidade e com uma equipe de pós vendas qualificada e responsiva
                            </p>
                            <v-btn
                                id="slide-text-btn"
                                :to="slide.btn_to"
                            >
                                {{ slide.btn_text }}
                                <v-icon>mdi mdi-arrow-right</v-icon>
                            </v-btn>
                        </div>
                    </v-row>
                </v-container>
            </v-carousel-item>
        </v-carousel>

        <!-- Botões -->
        <v-container>
            <v-row
                id="botoes"
            >
                <v-col>
                    <btnBox
                        cor="r"
                        icone="mdi mdi-instagram"
                        titulo="Instagram"
                        texto="Nos encontre também nas redes sociais."
                        caminho="https://www.instagram.com/triskeleletrificacao/"
                    />
                </v-col>
                <v-col>
                    <btnBox
                        cor="w"
                        icone="mdi mdi-linkedin"
                        titulo="Linkedin"
                        texto="Nos encontre também nas redes sociais."
                        caminho="https://www.linkedin.com/in/triskel-eletrifica%C3%A7%C3%A3o-e-automa%C3%A7%C3%A3o-518a721a6/"
                    />
                </v-col>
                <v-col>
                    <btnBox
                        cor="r"
                        icone="mdi mdi-whatsapp"
                        titulo="Whatsapp"
                        texto="Fale diretamente conosco: (14) 97709-5384"
                        caminho="https://api.whatsapp.com/send?phone=5514977095384&text=Olá"
                    />
                </v-col>
            </v-row>
        </v-container>

        <!-- Produtos -->
        <v-container
            align="start"
            justify="center"
        >
            <p
                id="titulo_prod"
                align="center"
            >
                Produtos
            </p>
            <prodTable />
        </v-container>

        <!-- Quem Somos -->
        <v-container
            id="quem_area"
        >
            <v-row
                class="d-flex flex-column align-center"
            >
                <h2 id="quem_titulo">
                    Quem Somos
                </h2>

                <barra />
            </v-row>
            <v-row>
                <p class="text-justify text-sm-center">
                    Com uma equipe que soma mais de 30 anos de experiência no mercado de
                    montagem de painéis, fundada em 2015, a Triskel nasceu para
                    acompanhar a evolução social e tecnológica em ressonância com a mutabilidade
                    constante das necessidades do mercado, desenvolvendo uma metodologia de trabalho
                    que prima, por meio de seu atendimento personalizado, pela confiança e parceria com
                    os clientes, bem como pelo foco nos resultados e maximização dos recursos, criando e
                    desenvolvendo soluções cada vez mais simplificadas e adequadas às necessidades dos
                    nossos clientes.
                </p>
            </v-row>
        </v-container>

        <!-- Endereço -->
        <v-container
            id="map_area"
        >
            <v-row>
                <v-col
                    id="map_text"
                    cols="12"
                    sm="4"
                >
                    <v-row
                        class="d-flex flex-column align-center"
                    >
                        <v-col
                            class="d-flex flex-column align-center"
                        >
                            <h2>Endereço</h2>
                            <barra />
                        </v-col>
                        <v-col>
                            <h4 align="center">
                                Est. Portão Honda, 3305  <br>
                                Jardim Revista  <br>
                                Suzano - SP
                            </h4>
                        </v-col>
                    </v-row>

                    <v-divider />

                    <v-row
                        class="d-flex flex-column align-center"
                    >
                        <v-col
                            class="d-flex flex-column align-center"
                        >
                            <h2>Contato</h2>
                            <barra />
                        </v-col>
                        <v-col>
                            <div align="center">
                                (11) 9 7709-5384<br>
                                vendas@triskeleletrificacao.com.br
                            </div>
                        </v-col>
                    </v-row>
                </v-col>

                <v-col
                    cols="12"
                    sm="8"
                >
                    <div id="map_map_map">
                        <iframe
                            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3658.6894775971746!2d-46.282636584878766!3d-23.507691665497955!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94ce79843d77f147%3A0x3234e2dca8bb2c74!2sEstr.%20Port%C3%A3o%20do%20Ronda%2C%203305%20-%20Jardim%20Europa%2C%20Suzano%20-%20SP%2C%2008696-043!5e0!3m2!1spt-BR!2sbr!4v1591809127611!5m2!1spt-BR!2sbr"
                            width="100%"
                            height="100%"
                            frameborder="0"
                            style="border:0;"
                            allowfullscreen=""
                            aria-hidden="false"
                            tabindex="0"
                        />
                    </div>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>

import btnBox from "~/components/btnBox.vue";
import prodTable from "~/components/prodTable.vue";
import barra from "~/components/barra.vue";

export default {
    components: {
        btnBox,
        prodTable,
        barra,
    },
    data () {
        return {
            slides: [
                {
                    img: "Imagens/Slides/slide1.png",
                    title: "O sucesso de um projeto, envolve a escolha do parceiro certo!",
                    btn_text: "Fale Conosco",
                    btn_to: "contato",
                },
                {
                    img: "Imagens/Slides/slide2.png",
                    title: "Conheça nossos produtos da linha de baixa tensão",
                    btn_text: "Produtos",
                    btn_to: "produtos",
                },
                {
                    img: "Imagens/Slides/slide3.png",
                    title: "Escolhendo sempre os melhores produtos para o seu projeto",
                    btn_text: "Fornecedores",
                    btn_to: "sobre",
                }
            ],
        };
    }
};
</script>

<style scoped>
  /* ---- Carrossel ---- */
  #slide {
    margin-bottom: 0px;
  }

  #slide-box {
    border-left: 10px solid #a91d21ff;
  }

  #slide-text-area {
    background-color: #000000c7;
    width: 70%;
    height: 100%;
  }

  #slide-text-welcome {
    color: #ff0000ff;
  }

  #slide-text-title {
    color:white;
    font:bold;
    font-size: 26pt;
  }

  #slide-text-text {
    color:white;
    font-size: 14pt;
  }

  #slide-text-btn {
    margin-top: 1%;
    background-color:#a91d21ff;
    color:white;
  }

  /* ---- Botões ---- */
  #botoes {
    margin-top: -100px;
  }

  /* ---- Produtos ---- */
  #titulo_prod {
    font-size: 25pt;
    color: #a91d21ff;
  }

  /* ---- Quem Somos ---- */
  #quem_area {
    background-color: #f2f2f2ff;
    color: black;
    padding-left: 10%;
    padding-right: 10%;
    text-align: center;
  }

  #quem_titulo {
    font-size: 20pt;
  }

  /* ---- Mapa ---- */
  #map_area {
    background-color: white;
  }

  #map_map_map {
    height: 100%;
    border-left: 10px solid;
    color: #a91d21ff;
  }

</style>