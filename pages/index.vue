<template>
 <v-carousel
    cycle
    height="550px"
    hide-delimiter-background
    show-arrows-on-hover
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
</template>



<script>
  export default {
    data () {
      return {
        slides: [
          {
            img: 'Imagens/Slides/slide1.png',
            title: "O sucesso de um proketo, envolve a escolha do parceiro certo!",
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
  }
</script>

<style scoped>
  #slide-box{
    padding-top: 5%;
    padding-left: 10%;
  }

  #slide-left-bar{
    background-color: #a91d21ff;
    width: 12px;
    height: 300px;
  }

  #slide-text-area{
    background-color: #000000c7;
    width: 600px;
    height: 300px;
    padding-left: 2%;
    padding-top: 1%;
  }

  #slide-text-welcome{
    color: #ff0000ff;
    font-size: 15pt;
    font:bold;
  }

  #slide-text-title{
    color:white;
    font:bold;
    font-size: 25pt;
  }

  #slide-text-text{
    color:white;
    font-size: 13pt;
  }

  #slide-text-btn{
    background-color:#a91d21ff;
    color:white;
  }
</style>