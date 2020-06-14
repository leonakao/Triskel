<template>
    <div>
        <!-- Root Element -->
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
</style>