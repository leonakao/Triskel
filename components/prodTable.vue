<template>
  <v-container>
    <v-row>
      <v-col
        v-for="(prod, n) in prods"
        :key="n"
      >
        <v-img
          :src="'Imagens/Produtos/'+prod.imagem+'.png'"
        />
        <p>{{prod.nome}}</p>

      </v-col>
    </v-row>
    <v-row>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        prods: [
          {
            imagem: 'Painel_de_distribuicao',
            nome:'Painéis de distribuição',
          },
          {
            imagem: 'QBGT',
            nome: 'Paineis gerais \"QGBT\"',
          },
          {
            imagem: 'Banco_de_capacitores',
            nome: 'Banco automático de capacitores',
          },
          {
            imagem: 'CCM',
            nome: 'Centro de controle de motores \"CCM\"'
          },
          {
            imagem: 'CLP',
            nome: 'Paineis de Automação \"CLP\"'
          },
          {
            imagem: 'OEM',
            nome: 'Soluções desenvolvidas para favricantes de equipamentos'
          },
          {
            imagem: 'Central_de_medicao',
            nome: 'Central de Medição'
          },
        ],
      }
    },
  }
</script>

<style scoped>

</style>