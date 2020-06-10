<template>
    <div>
        <!-- Root Element -->
        <v-container>
            <v-row>
                <v-col>
                    <v-img src="Imagens/prod.png">
                        <h1>Produtos</h1>
                    </v-img>
                </v-col>
            </v-row>
        </v-container>

        <v-container
            align="start"
            justify="center"
        >
            <prodTable />
        </v-container>
    </div>
</template>

<script>
import prodTable from "~/components/prodTable.vue";

export default {
    components: {
        prodTable,
    }
};
</script>

<style scoped>
  h1{
    color: white;
  }

  #titulo{
    align-items: center;
    justify-items: center;
  }
</style>