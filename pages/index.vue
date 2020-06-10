<template>
  <div>
   <!-- Carrossel -->

    <v-carousel
      cycle
      height="550px"
      hide-delimiters
      show-arrows-on-hover
      id="carrossel"
    >
      <v-carousel-item
        v-for="(slides, i) in slides"
        :key="i"
        :src="slides.img"
      >
        <v-container>
          <v-row id="slide-box">
            <div id="slide-left-bar"></div>
            <div id="slide-text-area">
              <p id="slide-text-welcome">Bem vindo a Triskel!</p>
              <p id="slide-text-title">{{slides.title}}</p>
              <p id="slide-text-text">Paineis elétricos de qualidade e com uma equipe de pós vendas qualificada e responsiva</p>
              <v-btn id="slide-text-btn"
                :to="slides.btn_to"
              >
                {{slides.btn_text}}
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
      >Produtos</p>
      <v-prodTable />
    </v-container>

  </div>
</template>

<script>

  import btnBox from "~/components/btnBox.vue";
  import prodTable from "~/components/prodTable.vue";

  export default {
    data () {
      return {
        slides: [
          {
            img: 'Imagens/Slides/slide1.png',
            title: "O sucesso de um projeto, envolve a escolha do parceiro certo!",
            btn_text: "Fale Conosco",
            btn_to: "contato",
          },
          {
            img: 'Imagens/Slides/slide2.png',
            title: "Conheça nossos produtos da linha de baixa tensão",
            btn_text: "Produtos",
            btn_to: "produtos",
          },
          {
            img: 'Imagens/Slides/slide3.png',
            title: "Escolhendo sempre os melhores produtos para o seu projeto",
            btn_text: "Fornecedores",
            btn_to: "sobre",
          }
        ],
      }
    },
    components: {
      btnBox
    }
  }
</script>

<style scoped>
  /* ---- style carrossel ---- */
  #slide{
    margin-bottom: 0px;
  }

  #slide-box{
    padding-top: 5%;
    padding-left: 10%;
  }

  #slide-left-bar{
    background-color: #a91d21ff;
    width: 12px;
    height: 350px;
  }

  #slide-text-area{
    background-color: #000000c7;
    width: 710px;
    height: 350px;
    padding-left: 2%;
    padding-top: 1%;
  }

  #slide-text-welcome{
    color: #ff0000ff;
    font-size: 18pt;
    font:bold;
  }

  #slide-text-title{
    color:white;
    font:bold;
    font-size: 26pt;
  }

  #slide-text-text{
    color:white;
    font-size: 14pt;
  }

  #slide-text-btn{
    margin-top: 20px;
    background-color:#a91d21ff;
    color:white;
  }

  /* ---- Botões ---- */
  #botoes{
    margin-top: -100px;
  }

  /* ---- Produtos ---- */
  #titulo_prod{
    font-size: 25pt;
    color: #a91d21ff;
  }

</style>