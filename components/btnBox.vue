<template>
    <div>
        <v-card
            :id="cor"
            :href="caminho"
            raised
            :height="tamanho"
        >
            <v-card-title>
                <v-icon
                    :id="cor+'_icon'"
                    size="200%"
                >
                    {{ icone }}
                </v-icon>

                <span
                    id="titulo"
                    class="pl-2"
                >{{ titulo }}</span>
            </v-card-title>
            <v-card-text :id="cor">
                {{ texto }}
            </v-card-text>
        </v-card>
    </div>
</template>

<script>
export default {
    props: {
        icone: {
            type: String,
            default:"",
        },
        titulo: {
            type: String,
            default:"",
        },
        texto: {
            type: String,
            default:"",
        },
        cor: {
            type: String,
            default:"w",
        },
        caminho: {
            type: String,
            default:"",
        },
    }
};
</script>

<style scoped>
  #w {
    background-color: white;
    color: black;
  }

  #w_icon {
    color:#a91d21ff;
  }

  #r {
    background-color: #a91d21ff;
    color: white;
  }

  #r_icon {
    color:white;
  }

</style>