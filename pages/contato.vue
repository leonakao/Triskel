<template>
    <div>
        <!-- Root Element -->

        <!-- Titulo -->
        <v-container>
            <v-row>
                <v-col>
                    <v-img
                        src="Imagens/sobre.png"
                        class="align-center text-center"
                    >
                        <h1 id="titulo_page">
                            Contato
                        </h1>
                    </v-img>
                </v-col>
            </v-row>
        </v-container>

        <!-- Botões -->
        <v-container>
            <v-row id="botao">
                <v-col>
                    <btnBox
                        cor="r"
                        icone="mdi mdi-map-marker"
                        titulo="Pessoalmente"
                        texto="Est. Portão Honda, 3305, Jardim Revista, Suzano - SP"
                    />
                </v-col>
                <v-col>
                    <btnBox
                        cor="w"
                        icone="mdi mdi-email"
                        titulo="E-mail"
                        texto="Entre em contato: vendas@triskeleletrificacao.com.br"
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

        <!-- Mapa -->
        <v-container>
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
        </v-container>
    </div>
</template>

<script>
import btnBox from "~/components/btnBox.vue";

export default {
    components:{
        btnBox,
    }
};
</script>

<style scoped>
    /* ---- Geral ---- */
    #c {
        color: #a91d21ff;
    }

    /* ---- Titulo ---- */
    #titulo_page {
        color: white;
    }

    /* ---- Botões ---- */
    #botao {
        margin-top: -3%;
    }
</style>