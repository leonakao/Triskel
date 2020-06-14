<template>
    <div>
        <!-- Rooter Element -->
        <!-- Carrossel -->

        <v-carousel
            cycle
            hide-delimiters
            show-arrows-on-hover
        >
            <v-carousel-item
                v-for="(slide, i) in slides"
                :key="i"
                :src="slide.img"
            >
                <v-container>
                    <v-row
                        id="slide-box"
                    >
                        <v-col
                            id="slide-text-area"
                            sm="8"
                            cols="12"
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
                        </v-col>
                    </v-row>
                </v-container>
            </v-carousel-item>
        </v-carousel>

        <!-- Botões -->
        <v-container>
            <v-row
                id="botoes"
            >
                <v-col
                    cols="12"
                    sm="4"
                >
                    <btnBox
                        cor="r"
                        icone="mdi mdi-flash"
                        titulo="Produtos"
                        texto="Encontre o melhor produto para seu projeto."
                        to="produtos"
                    />
                </v-col>
                <v-col
                    cols="12"
                    sm="4"
                >
                    <btnBox
                        cor="w"
                        icone="mdi mdi-briefcase"
                        titulo="Venha nos conhecer"
                        texto="Conheça seu futuro parceiro nos negócios."
                        to="sobre"
                    />
                </v-col>
                <v-col
                    cols="12"
                    sm="4"
                >
                    <btnBox
                        cor="r"
                        icone="mdi mdi-comment-processing-outline"
                        titulo="Fale conosco"
                        texto="Mande-nos seu projeto"
                        to="contato"
                    />
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>

import btnBox from "~/components/btnBox.vue";

export default {
    components: {
        btnBox,
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
  #slide-box {
    border-left: 10px solid #a91d21ff;
    margin-left: 10%;
    margin-top: 5%;
  }

  #slide-text-area {
    background-color: #000000c7;
    padding-left: 2%;
  }

  #slide-text-welcome {
    color: #ff0000ff;
  }

  #slide-text-title {
    color:white;
    font:bold;
    font-size: 200%;
  }

  #slide-text-text {
    color:white;
    font-size: 125%;
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

</style>

<!-- Recomendações amanda
- Aumentar o espaçamento entre as partes do site
- Aplicar grid em tudo

-->