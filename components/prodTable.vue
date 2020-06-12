<template>
    <v-container>
        <v-row>
            <v-col
                v-for="(prod, n) in prods"
                :key="n"
                cols="6"
                sm="2"
            >
                <v-img
                    :src="'Imagens/Produtos/'+prod.imagem+'.png'"
                />

                <h3
                    id="texto"
                    align="center"
                >
                    {{ prod.nome }}
                </h3>
            </v-col>
        </v-row>
        <v-row />
    </v-container>
</template>

<script>
export default {
    data () {
        return {
            prods: [
                {
                    imagem: "Painel_de_distribuicao",
                    nome:"Painéis de Distribuição",
                },
                {
                    imagem: "QBGT",
                    nome: "Paineis Gerais \"QGBT\"",
                },
                {
                    imagem: "Banco_de_capacitores",
                    nome: "Banco Automático de Capacitores",
                },
                {
                    imagem: "CCM",
                    nome: "Centro de Controle de Motores \"CCM\""
                },
                {
                    imagem: "CLP",
                    nome: "Paineis de Automação \"CLP\""
                },
                {
                    imagem: "OEM",
                    nome: "Soluções Desenvolvidas Para Fabricantes de Equipamentos"
                },
                {
                    imagem: "Central_de_medicao",
                    nome: "Central de Medição"
                },
            ],
        };
    },
};
</script>

<style scoped>
  #texto{
    color: black;
    }
</style>

